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

<details>
<summary>Details and Commentary</summary>

* **Time and tasks assigned:** Who assign any time to every team member to work on specific tasks is the own team. The one to assign the task to every team member to work, in the same way as the time, also the own team is the one who does this to work on each specific task.

</details>


> [!WARNING]
> **El antipatrón del "Project Manager con sombrero de Scrum Master"**  
> Forzar a un PM tradicional a actuar como Scrum Master manteniendo una mentalidad de comando y control destruye la autoorganización del equipo. El SM debe facilitar que el equipo tome decisiones, no asignárselas de arriba hacia abajo.

---

## Glosario General de Conceptos

Para garantizar una única fuente de verdad y facilitar el acceso a todas las definiciones del playbook, el glosario de términos clave se ha centralizado en el archivo principal en la raíz:

👉 **[Glosario General del Playbook](../GLOSSARY.md)**

