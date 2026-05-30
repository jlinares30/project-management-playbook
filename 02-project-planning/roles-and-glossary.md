# Comparación de Roles y Glosario Cruzado de Conceptos

> [!NOTE]
> **Enfoque de Ingeniería y Liderazgo Técnico (Big Tech Mindset)**  
> Uno de los mayores fallos en el diseño organizacional de proyectos es mapear directamente roles antiguos a marcos modernos sin entender su cambio de filosofía. En Big Tech, las responsabilidades de planificación y liderazgo están distribuidas en lugar de concentrarse en un único individuo. Entender quién toma qué decisiones es clave para resolver preguntas de diseño de sistemas y de comportamiento organizacional.

---

## Comparativa de Roles: Predictivo (PMBOK) vs. Adaptativo (Ágil/Scrum)

En la gestión tradicional (PMBOK), el **Project Manager (PM)** es la figura central y el responsable final de equilibrar el alcance, el tiempo, el costo y la asignación del equipo. En Agile (Scrum), estas responsabilidades se dividen en tres figuras distintas para balancear la visión del negocio, la facilitación de los procesos y la excelencia técnica.

| Dimensión de Responsabilidad | Enfoque Predictivo (PMBOK) | Enfoque Adaptativo (Scrum/Agile) |
| :--- | :--- | :--- |
| **Definición del "Qué" y "Por qué"** | **Project Manager + Sponsor:** Traducen las especificaciones iniciales y limitan los cambios en el alcance. | **Product Owner (PO):** Es el único dueño del Product Backlog, prioriza según el valor comercial y decide qué construir. |
| **Gobernanza del Proceso** | **Project Manager:** Asegura el cumplimiento de las fases de planificación, ejecución y reporte de estado. | **Scrum Master (SM):** Líder sirviente que enseña y facilita el marco ágil, remueve impedimentos y protege la autonomía del equipo. |
| **Diseño y Ejecución Técnica ("Cómo")** | **Líder Técnico / Arquitecto:** Asigna tareas a los miembros del equipo y controla el cumplimiento del diseño. | **Developers (Dev Team):** Autoorganizados y multifuncionales. Definen de manera conjunta las estimaciones y la arquitectura técnica. |
| **Gestión del Presupuesto (Costo)** | **Project Manager:** Monitorea desvíos monetarios mediante el cálculo clásico de líneas base (EVM). | **Product Owner + Sponsor:** Definen y gestionan la capacidad total financiada por Sprint o Release. |
| **Resolución de Impedimentos** | **Project Manager:** Escala y gestiona solicitudes formales de recursos o cambios a gerentes funcionales. | **Scrum Master:** Resuelve bloqueos de forma inmediata facilitando interacciones rápidas y eliminando burocracia. |

### Matriz de Equivalencias (Peligro de Mapeo Directo)

```text
  TRADICIONAL (PMBOK)                         ÁGIL (Scrum)
  ┌─────────────────┐                        ┌─────────────────┐
  │ Project Manager │ ─── ¿Equivale a...? ──> │ Scrum Master    │ (ERROR: El SM no asigna tareas)
  └─────────────────┘                        └─────────────────┘
                                             ┌─────────────────┐
                                             │ Product Owner   │ (ERROR: El PO no define la técnica)
                                             └─────────────────┘
```

> [!WARNING]
> **El antipatrón del "Project Manager con sombrero de Scrum Master"**  
> Forzar a un PM tradicional a actuar como Scrum Master manteniendo una mentalidad de comando y control destruye la autoorganización del equipo. El SM debe facilitar que el equipo tome decisiones, no asignárselas de arriba hacia abajo.

---

## Glosario General de Conceptos (Con Enlaces Cruzados)

A continuación se presenta un glosario de términos clave utilizados a lo largo de este playbook. Cada término está referenciado directamente a su documento técnico de desarrollo para facilitar tu estudio.

### A
* **[Aseguramiento de la Calidad (QA)](../03-software-quality-standards/agile-quality-management.md)**: Enfoque preventivo orientado a procesos para evitar que surjan defectos en el código.
* **[Agile EVM (Earned Value Management)](../02-project-planning/agile-cost-management.md)**: Técnica adaptativa para medir el progreso real del proyecto comparando los puntos de historia completados frente al Release Plan.

### B
* **[Brooks' Law (Ley de Brooks)](../02-project-planning/agile-cost-management.md)**: Principio que postula que añadir desarrolladores a un proyecto de software retrasado suele retrasarlo aún más a corto plazo.
* **[Built-in Quality (Calidad Integrada)](../README.md)**: Disciplina diaria que asegura que la calidad no es una fase final de inspección, sino una práctica de ingeniería integrada desde el diseño inicial.
* **[Burn-down Chart](../01-agile-frameworks/agile-metrics.md)**: Gráfico de trabajo pendiente que muestra la trayectoria diaria de los puntos de historia restantes dentro de un Sprint.

### C
* **[Capacity-Based Funding](../02-project-planning/agile-cost-management.md)**: Método de financiamiento ágil que estabiliza los costos financiando equipos de desarrollo fijos y dedicados en lugar de estimar tareas por separado.
* **[Control de Calidad (QC)](../03-software-quality-standards/agile-quality-management.md)**: Práctica correctiva orientada a producto enfocada en la detección e inspección de errores en software ya construido.
* **[Cycle Time (Tiempo de Ciclo)](../01-agile-frameworks/agile-metrics.md)**: Tiempo total transcurrido desde que el equipo comienza a trabajar activamente en una tarea hasta que se completa.

### D
* **[Definition of Done (DoD)](../01-agile-frameworks/scrum-and-kanban.md)**: Conjunto de criterios de calidad explícitos y acordados que debe cumplir una historia de usuario para considerarse completada.
* **[Dependencia Obligatoria](../01-agile-frameworks/agile-schedule-management.md)**: Relación secuencial ineludible por la naturaleza física o lógica del desarrollo de software.

### E
* **[EDT / WBS (Estructura de Desglose de Trabajo)](scope-and-wbs.md)**: Descomposición jerárquica orientada al entregable de todo el trabajo necesario para completar el proyecto.
* **[Epic (Épica)](../01-agile-frameworks/user-stories-discovery.md)**: Historia de usuario muy grande que debe ser desglosada en tareas más pequeñas para poder completarse en un único Sprint.

### G
* **[Gherkin (BDD)](../01-agile-frameworks/user-stories-discovery.md)**: Lenguaje estructurado estructurado en la sintaxis *Given-When-Then* que permite describir los criterios de aceptación en un formato comprensible para el negocio y automatizable.

### I
* **[INVEST](../01-agile-frameworks/user-stories-discovery.md)**: Acrónimo de criterios de calidad para escribir historias de usuario (Independiente, Negociable, Valiosa, Estimable, Pequeña, Verificable).

### L
* **[Lead Time (Tiempo de Entrega)](../01-agile-frameworks/agile-metrics.md)**: Tiempo transcurrido desde que una solicitud o idea ingresa al backlog hasta que se entrega en producción al usuario.
* **[Líder Sirviente (Servant Leader)](agile-resource-management.md)**: Filosofía de liderazgo enfocada en habilitar el éxito del equipo, remover impedimentos y facilitar su crecimiento en lugar de ejercer control autoritario.

### M
* **[MVP (Producto Mínimo Viable)](scope-and-wbs.md)**: Enfoque de Henrik Kniberg orientado a entregar la versión de producto más pequeña que sea Testable, Usable y Lovable para validar hipótesis comerciales.

### P
* **[Post-Mortem (Blameless)](../05-case-studies-templates/post-mortem-template.md)**: Plantilla y proceso de análisis retrospectivo enfocado en identificar las causas raíz de fallas en producción sin buscar culpables individuales.
* **[Project Charter Dinámico](agile-integration-management.md)**: Acta de constitución de proyecto ágil que actúa como un artefacto vivo enfocado en la visión y metas, permitiendo flexibilidad de alcance.

### R
* **[Release Plan (Plan de Lanzamiento)](../01-agile-frameworks/agile-schedule-management.md)**: Hoja de ruta ágil de alto nivel que proyecta qué funcionalidades se entregarán en una serie de iteraciones futuras.

### T
* **[Transferencia de Conocimiento Tácito](agile-integration-management.md)**: El intercambio de habilidades complejas y "know-how" no documentables mediante interacciones directas como pair programming o code reviews.

### V
* **[Velocity (Velocidad)](../01-agile-frameworks/agile-metrics.md)**: Medida del rendimiento histórico del equipo Scrum expresada en puntos de historia completados en promedio por Sprint.
