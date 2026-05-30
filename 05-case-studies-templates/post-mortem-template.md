# Plantilla de Análisis de Incidente Post-Mortem

**ID de Incidente**: `#INC-YYYY-XXXX`  
**Título del Incidente**: `[Breve descripción, ej. Caída del servidor de pasarela de pago]`  
**Fecha del Incidente**: `[DD/MM/AAAA]`  
**Autor(es)**: `[Nombre(s)]`  
**Estado**: `[Borrador / Completado / En Revisión]`  

---

## 1. Resumen Ejecutivo (TL;DR)
*Un resumen de 3 a 5 líneas de lo que sucedió, el impacto comercial directo y la solución final aplicada.*

* **Severidad**: Crítica / Mayor / Menor  
* **Tiempo Total de Inactividad (Downtime)**: `[X horas, Y minutos]`  
* **Impacto Comercial**: `[Ej. 250 compras fallidas, $5,000 USD estimados en pérdidas]`  

---

## 2. Impacto en los Usuarios y Métricas
*Detalle cuantitativo del impacto en clientes, APIs externas y rendimiento del sistema.*

* **Usuarios afectados**: `[Cantidad o % del total]`  
* **Métricas de soporte**: `[Incremento en tickets de soporte, llamadas]`  
* **Gráficos clave**: *(Inserta capturas de pantalla de tus paneles de monitoreo Datadog/Grafana si aplica)*  

---

## 3. Cronología de los Hechos (Timeline)
*Detalle minuto a minuto de cómo se desarrolló el incidente desde el inicio hasta la restauración completa.*

* **14:00** - El sistema de alertas automáticas detecta un pico inusual de errores HTTP 500 en `/api/payments`.
* **14:05** - El equipo de guardia (On-call) recibe la alerta e inicia la investigación.
* **14:15** - Se identifica que el problema se debe a un cambio de configuración en la clave de la API del proveedor de pagos durante el despliegue de las 13:55.
* **14:20** - Se inicia el rollback de la configuración a la versión anterior.
* **14:25** - Despliegue de rollback completado con éxito. Los errores HTTP 500 se reducen a 0.
* **14:30** - Incidente cerrado oficialmente. Monitoreo pasivo activado.

---

## 4. Análisis de Causa Raíz (Los 5 Porqués)
*Preguntar "Por qué" iterativamente para encontrar la causa raíz subyacente y evitar soluciones superficiales.*

1. **¿Por qué fallaron los pagos?**  
   Porque la API de pagos del backend recibió credenciales incorrectas.
2. **¿Por qué las credenciales eran incorrectas?**  
   Porque la variable de entorno de producción fue sobreescrita con la clave de staging en el último despliegue.
3. **¿Por qué se sobreescribió con la clave de staging?**  
   Porque el script de despliegue automatizado no diferenció las variables por rama de origen de manera correcta.
4. **¿Por qué el script no diferenció las ramas?**  
   Porque el archivo de configuración de CI/CD fue modificado el día anterior por un desarrollador para realizar una prueba rápida y no fue revisado por pares.
5. **¿Por qué no fue revisado por pares?** (Causa Raíz)  
   Porque la rama de configuración del pipeline de CI/CD no tiene políticas de protección de ramas activas ni revisiones obligatorias.

---

## 5. Acciones Correctivas y Preventivas (Action Items)

| ID | Acción Recomendada | Tipo | Responsable | Fecha Límite |
| :--- | :--- | :---: | :--- | :--- |
| **ACT-01** | Proteger la rama de CI/CD con revisión obligatoria de pull requests. | Preventiva | `[Nombre]` | `[DD/MM/AAAA]` |
| **ACT-02** | Separar los secretos de producción de los de staging en bóvedas seguras (ej. AWS Secrets Manager). | Mitigación | `[Nombre]` | `[DD/MM/AAAA]` |
| **ACT-03** | Crear una prueba de integración básica de salud (*smoke test*) posdespliegue que valide la conectividad con Stripe. | Preventiva | `[Nombre]` | `[DD/MM/AAAA]` |
