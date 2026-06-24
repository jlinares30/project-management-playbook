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

---

## Particularidades de la Comunicación Ágil

En los entornos ágiles, la comunicación no es solo un proceso de reporte formal, sino una herramienta de colaboración diaria continua centrada en las personas.

### 1. Enfoque Predictivo vs. Ágil
* **Predictivo:** Comunicación formal, altamente estructurada y basada en un plan estricto preestablecido (reportes periódicos y actas de reunión oficiales).
* **Ágil:** Comunicación continua, colaborativa y orgánica. Se enfoca en las interacciones diarias cara a cara y en ciclos rápidos de retroalimentación por encima de procesos y herramientas rígidas.

### 2. Canales: Sincrónica vs. Asincrónica
Para una comunicación eficiente, el equipo debe balancear ambos tipos de comunicación:
* **Sincrónica (Reuniones directas, llamadas, videollamadas):** Ideal para toma de decisiones rápidas, resolución de conflictos y alineación inmediata. Las ceremonias ágiles (Daily Scrum, Sprint Planning, Sprint Review, Sprint Retrospective) son los espacios sincrónicos principales.
* **Asincrónica (Chats tipo Slack, comentarios en Jira, correos):** Ideal para actualizaciones técnicas de menor urgencia, intercambio de documentación y permitir que los ingenieros tengan largos periodos de trabajo ininterrumpido (*deep work*).

### 3. Radiadores de Información
En lugar de ocultar la información en reportes complejos, los equipos ágiles utilizan **radiadores de información** visibles y accesibles para cualquiera:
* **Tablero Kanban/Scrum:** Muestra el flujo y estado real del trabajo actual.
* **Burndown / Burnup Charts:** Gráficos que visualizan el progreso y ritmo del sprint o release.
* **Tablero de Impedimentos (Impediment Board):** Visibilidad pública sobre qué bloquea al equipo y quién está a cargo de solucionarlo.

### 4. Indicadores de Evaluación de la Comunicación
Para medir la efectividad de los canales de comunicación, el Scrum Master o Agile Coach evalúa:
* **Efectividad del flujo de información:** ¿Se comparte la información crítica a tiempo?
* **Resolución ágil de conflictos:** ¿Los bloqueantes y diferencias se discuten y resuelven rápidamente?
* **Participación activa:** ¿Los miembros del equipo y stakeholders asisten y aportan valor en las ceremonias sincrónicas?

### 5. Equipos Distribuidos (Desafíos y Buenas Prácticas)
Cuando el equipo de desarrollo trabaja de manera remota o deslocalizada:
* **Barreras comunes:** Diferencias de zona horaria, barreras del idioma y problemas de conectividad o infraestructura.
* **Soluciones ágiles:**
  * **Acuerdos de equipo (Working Agreements):** Definición clara de horarios de solapamiento común y reglas para reuniones.
  * **Herramientas de colaboración visual:** Pizarras virtuales interactivas (Miro, FigJam) y repositorios centralizados actualizados.
  * **Reglas de reunión:** Cámaras encendidas durante sesiones clave, minutas auto-documentadas en la wiki del proyecto.

---

## Caso Práctico: Desafíos de Comunicación y Rol del Product Owner

### Contexto del Escenario:
Un equipo de desarrollo ágil que trabaja en un sistema de reservas en línea experimenta las siguientes dificultades:
1. **Poca asistencia del Product Owner (PO):** El PO casi no asiste a las Daily Scrum, y cuando participa, no resuelve las dudas técnicas en el momento, obligando al equipo a tomar decisiones basadas en supuestos.
2. **Requisitos de forma externa:** El PO suele enviar correos electrónicos fuera del horario laboral con cambios sustanciales en los requerimientos, sin discutirlos en las sesiones de equipo, lo cual genera reprocesos (*rework*) y frustración técnica.

### Análisis y Acciones Ágiles Propuestas:

Para mitigar y resolver estas fallas de comunicación basadas en principios ágiles, se acuerda implementar dos acciones concretas de inmediato:

#### Acción 1: Re-establecer los Acuerdos de Trabajo del Product Owner
* **Enfoque:** Conversar de forma transparente en la Retrospectiva y establecer con el PO que el Daily Scrum es el foro principal de alineación diaria (o bien definir un espacio fijo de 15 minutos diario de QA con el PO si no puede asistir al Daily).
* **Meta:** Lograr que las dudas técnicas críticas que bloquean el desarrollo tengan un tiempo máximo de respuesta pactado (SLA de resolución de dudas técnicas, ej. máximo 4 horas).

#### Acción 2: Control de Cambios en Iteración y Eliminación del Correo como Canal de Requisitos
* **Enfoque:** Acordar que **ningún cambio de alcance se realiza a través de correo electrónico**. Los correos electrónicos nocturnos se considerarán propuestas o ideas a evaluar, pero no requerimientos válidos para el sprint en curso.
* **Meta:** Todo cambio de alcance debe ingresarse en el *Product Backlog*, evaluarse en la sesión de *Backlog Refinement* o planificación del siguiente sprint, y priorizarse comparándolo con el valor de las otras tareas. Durante un sprint activo, el alcance debe protegerse contra cambios disruptivos no acordados con el equipo.

