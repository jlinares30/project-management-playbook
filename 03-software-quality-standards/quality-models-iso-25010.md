# ISO/IEC 25010: Modelos de Calidad del Producto de Software

El estándar **ISO/IEC 25010** define un modelo para evaluar la calidad del producto de software a través de 8 características principales y múltiples subcaracterísticas de calidad.

---

## Modelo de Calidad del Producto

A continuación se detallan las características que determinan la calidad técnica y funcional del software:

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│                            Calidad de Software                              │
├───────────────┬────────────────┬──────────────┬───────────────┬─────────────┤
│Adecuación     │Eficiencia de   │Compatibilidad│Usabilidad     │Fiabilidad   │
│Funcional      │Rendimiento     │              │               │             │
├───────────────┼────────────────┼──────────────┴───────────────┼─────────────┤
│Seguridad      │Mantenibilidad  │Portabilidad                  │             │
└───────────────┴────────────────┴──────────────────────────────┴─────────────┘
```

---

## Análisis de Características Clave y Métricas Asociadas

### 1. Mantenibilidad (Maintainability)
Es la facilidad con la que el software puede modificarse, corregirse o mejorarse.
* **Modularidad**: Grado en que los módulos individuales son independientes (bajo acoplamiento, alta cohesión).
* **Reusabilidad**: Grado en que un activo puede usarse en múltiples sistemas.
* **Analizabilidad**: Facilidad para diagnosticar deficiencias o fallas a partir de logs y trazas.
* **Modificabilidad**: Capacidad de realizar cambios en el código sin introducir regresiones o bugs colaterales.
* **Métrica clave**: *Índice de Mantenibilidad (Maintainability Index)* de 0 a 100 y *Deuda Técnica* en días u horas.

### 2. Seguridad (Security)
Grado en que el software protege la información y los datos de accesos no autorizados.
* **Confidencialidad**: Acceso exclusivo a usuarios autorizados.
* **Integridad**: Prevención de alteraciones no autorizadas de datos.
* **No repudio**: Imposibilidad de negar haber realizado una acción en el sistema (trazabilidad y auditoría).
* **Autenticidad**: Validación inequívoca de la identidad del usuario o servicio.
* **Métrica clave**: *Número de vulnerabilidades críticas abiertas (OWASP Top 10)*.

### 3. Eficiencia de Rendimiento (Performance Efficiency)
Relación entre el nivel de rendimiento del software y los recursos físicos consumidos.
* **Comportamiento temporal**: Tiempos de respuesta y procesamiento del sistema.
* **Utilización de recursos**: Consumo de CPU, memoria y ancho de banda.
* **Capacidad**: Límites del sistema (ej. máximo número de transacciones por segundo o usuarios concurrentes).
* **Métrica clave**: *Tiempo de respuesta promedio (Response Time)* y *Tasa de error bajo carga*.

### 4. Fiabilidad (Reliability)
Grado en que el sistema realiza sus funciones bajo condiciones específicas y durante un período de tiempo definido.
* **Madurez**: Frecuencia con la que falla el sistema debido a bugs.
* **Tolerancia a fallos**: Capacidad de operar ante fallas de componentes de infraestructura o servicios externos.
* **Recuperabilidad**: Habilidad para recuperar datos y restablecer el estado operativo tras una falla.
* **Métrica clave**: *MTBF (Mean Time Between Failures)* y *MTTR (Mean Time To Repair)*.
