# Gestión de Interesados (Stakeholders) y Comunicación

La comunicación efectiva es el pegamento de los proyectos. Mantener a los interesados informados con el nivel adecuado de detalle evita malentendidos y garantiza el apoyo continuo al proyecto.

---

## Matriz de Poder e Interés (Gobernanza de Interesados)

No todos los interesados requieren el mismo nivel de comunicación. Los clasificamos en cuatro cuadrantes según su nivel de poder de decisión e interés en el proyecto:

```text
       Poder Alto
          ^
          |  Mantener Satisfechos        |  Gestionar de Cerca (Socios)
          |  (Ej. Reguladores de QA,     |  (Ej. Patrocinador/Sponsor,
          |   Directores de TI)          |   Product Owner principal)
          |                              |
          +------------------------------+------------------------------> Interés Alto
          |                              |
          |  Monitorear (Mínimo Esfuerzo)|  Mantener Informados
          |  (Ej. Usuarios indirectos,   |  (Ej. Equipo de ventas,
          |   Proveedores externos)      |   Usuarios finales activos)
          |
```

* **Gestionar de Cerca**: Involucrarlos activamente. Reuniones presenciales o reportes semanales directos.
* **Mantener Satisfechos**: Cumplir sus requerimientos de control y gobernanza. Evitar saturación.
* **Mantener Informados**: Actualizaciones periódicas ligeras (ej. boletín de lanzamiento mensual o dashboards auto-servicio).
* **Monitorear**: Comunicación pasiva o bajo demanda.

---

## Plan de Comunicación del Proyecto

| Canal / Reunión | Frecuencia | Audiencia | Objetivo | Formato |
| :--- | :--- | :--- | :--- | :--- |
| **Comité de Dirección (Steering Committee)** | Mensual | Sponsor, PM, Clientes clave | Reportar hitos de alto nivel, estado financiero e hitos del Roadmap. | Presentación ejecutiva (PDF) |
| **Reporte de Estado Semanal** | Semanal (Viernes) | Interesados de nivel medio y equipo | Visibilidad del avance del proyecto, riesgos bloqueantes y entregables inmediatos. | Correo electrónico / Documento resumido |
| **Sprint Review** | Fin de Sprint (cada 2 sem.) | Usuarios finales, PO, Desarrolladores | Demo en vivo de la funcionalidad útil completada en el Sprint para recibir feedback. | Sesión síncrona interactiva |

---

## Plantilla de Reporte de Estado Semanal (Weekly Status Report)

**Proyecto**: `[Nombre del Proyecto]`  
**Período**: `[DD/MM/AAAA - DD/MM/AAAA]`  
**Líder de Proyecto**: `[Nombre de PM]`  
**Estado General**: **Verde** / **Amarillo** / **Rojo**

---

### Resumen Ejecutivo
*Breve descripción de 2-3 líneas sobre el estado general del proyecto.*

### Hitos Alcanzados esta Semana
* **[Entregable 1]**: *Descripción del hito completado (ej. Despliegue de pasarela de pago en staging).*
* **[Entregable 2]**: *Descripción (ej. Aprobación del diseño UX por el Sponsor).*

### Tareas Planificadas para la Próxima Semana
* **[Entregable 3]**: *Meta de desarrollo.*
* **[Entregable 4]**: *Pruebas de carga e infraestructura.*

### Riesgos y Bloqueantes Activos
* **[Bloqueante 1]**: *Detalle del impedimento y quién es el responsable de resolverlo para no impactar la ruta crítica.*
