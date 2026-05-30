# Gestión de la Calidad en Proyectos Ágiles

> [!NOTE]
> **Enfoque de Ingeniería y Liderazgo Técnico (Big Tech Mindset)**  
> En Big Tech, la calidad del software no es responsabilidad exclusiva de un departamento de "QA/Testing". Se adopta la cultura de "Calidad Integrada" (*Built-in Quality*), donde los ingenieros de desarrollo son dueños del testing automatizado de su propio código, y las prácticas de integración continua (CI) actúan como el árbitro objetivo de calidad antes de cualquier mezcla de código.

---

## Calidad en Cascada vs. Calidad en Agile

En la gestión tradicional en cascada (*Waterfall*), la calidad se concibe como una fase final del ciclo de vida del software, ubicada justo antes del despliegue. En Agile, la calidad es una disciplina continua e iterativa que empieza desde la reunión de planificación (Sprint Planning) hasta la demo final.

```text
  TRADICIONAL (Cascada):
  [Requisitos] ──> [Diseño] ──> [Desarrollo] ──> [Pruebas / QA] (Fase final de alto estrés)

  ÁGIL:
  En cada Sprint (1-4 semanas):
  [Planificación] ──> [Desarrollo + Testing Unitario & Regresión] ──> [Demo (UAT)] ──> [Retrospectiva]
```

---

## Aseguramiento de Calidad (QA) vs. Control de Calidad (QC)

Es común confundir estos términos, pero un consultor experto debe mapearlos con precisión:

| Dimensión | Aseguramiento de Calidad (QA - Quality Assurance) | Control de Calidad (QC - Quality Control) |
| :--- | :--- | :--- |
| **Enfoque** | Orientado a **procesos** y prevención de defectos. | Orientado a **productos** y detección de errores. |
| **Acción** | Preventiva: define cómo codificar y probar para evitar que surjan bugs (ej. linters, pair programming). | Correctiva: inspecciona el código ya terminado para encontrar fallos (ej. ejecución de pruebas manuales). |
| **Responsabilidad** | Todo el equipo de ingeniería (incluyendo desarrolladores y arquitectos). | Tradicionalmente asignado a testers/QA dedicados independientes. |
| **Antipatrón Común** | Creer que "QA" es solo correr pruebas manuales al final del Sprint. | Dejar que los desarrolladores entreguen código roto asumiendo que "QA lo encontrará". |

* **Consolidación en Agile:** Los especialistas en calidad participan desde el inicio del Sprint escribiendo los criterios de aceptación (Gherkin/BDD) y ayudando a diseñar la arquitectura de pruebas antes de que se escriba el código base.

---

## Estrategia de Validación Interna en la Iteración

Para garantizar la estabilidad del software, el equipo ejecuta una suite automatizada de validaciones con diferentes cadencias:

1. **Daily Builds (Compilaciones Diarias):** Compilación e integración automática del código de todas las ramas en un servidor central.
2. **Smoke Tests (Pruebas de Humo):** Suite de pruebas ultra rápida (usualmente unitarias y de API clave) que se ejecuta en cada *Pull Request* para validar que las funciones críticas no estén rotas.
3. **Pruebas de Regresión Automatizadas:** Suite extensa que valida que el software existente no se haya roto tras añadir nuevas funcionalidades. Se ejecutan automáticamente en el pipeline de CI antes del despliegue en Staging o Producción.
4. **User Acceptance Tests (UAT):** Validación final por parte de los usuarios de negocio o el PO al final de la iteración para confirmar el cumplimiento de las expectativas.

---

> [!TIP]
> **Pregunta de Entrevista de Big Tech (Technical Leadership & Quality)**  
> *En tu equipo de ingeniería, los desarrolladores están entregando historias de usuario completas a producción de forma rápida, pero el porcentaje de regresiones y bugs en producción ha subido un 20%. Los desarrolladores culpan al equipo de testing por "no probar lo suficiente". ¿Cómo solucionas esta fricción cultural y técnica?*
> 
> **Respuesta Estratégica:**  
> 1. **Eliminar el antipatrón de "QA como red de seguridad":** Reúno al equipo y aclaro que la calidad es responsabilidad exclusiva del creador del código. El equipo de desarrollo es dueño de sus pruebas unitarias y de integración. Si un bug llega a producción, es un fallo del proceso de ingeniería, no del equipo de testing.
> 2. **Implementar "Quality Gates" en el Pipeline de CI/CD:**
>    * Configuro reglas estrictas en GitHub: Cobertura mínima de código nuevo del 80% antes de permitir el merge.
>    * Ejecución obligatoria de la suite de regresión automática en cada Pull Request.
> 3. **Shift-Left Testing (Mover las pruebas a la izquierda):** Involucro al ingeniero de QA/Testing en las fases de refinamiento y diseño técnico. Antes de escribir código, el desarrollador y el QA acuerdan los casos de prueba en formato BDD. Esto asegura que el desarrollador programe teniendo claros los límites de aceptación (*Test-Driven Development / Behaviour-Driven Development*).
