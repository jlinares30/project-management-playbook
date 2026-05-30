# Playbook de Gestión de Proyectos y Calidad de Software

> [!NOTE]
> **Manifiesto de Gestión y Control de Calidad**  
> *"La calidad no es un accidente; es siempre el resultado de un esfuerzo de la inteligencia y una ejecución disciplinada."*

Bienvenido a tu repositorio centralizado de conocimiento. Este playbook reúne metodologías ágiles, buenas prácticas de ingeniería de software, estándares internacionales de calidad y plantillas listas para su aplicación en el ciclo de vida del desarrollo.

---

## Estructura del Playbook

```text
├── README.md                      # Manifiesto de gestión y control de calidad
├── 01-agile-frameworks/           # Metodologías y Entrega de Valor
│   ├── scrum-and-kanban.md        # Roles, ceremonias y cuándo usar cada flujo
│   ├── user-stories-discovery.md  # Criterios de aceptación (Gherkin/BDD) y Story Mapping
│   └── agile-metrics.md           # Velocity, Lead Time, Cycle Time y Burn-down charts
├── 02-project-planning/           # Gestión del Alcance y Gobernanza
│   ├── scope-and-wbs.md           # Estructura de Desglose de Trabajo (EDT/WBS)
│   ├── risk-management.md         # Matriz de riesgos (Mitigación de fallas en proyectos)
│   └── stakeholders-comm.md       # Gestión de expectativas y reportes de estado
├── 03-software-quality-standards/ # Estándares y Gobernanza Técnica
│   ├── iso-iec-12207.md           # Ciclo de vida del software (Procesos base)
│   └── quality-models-iso-25010.md# Atributos de calidad (Mantenibilidad, Seguridad, Eficiencia)
├── 04-testing-strategies/         # Estrategias de Validación (El núcleo de Calidad)
│   ├── testing-pyramid.md         # Unit, Integration, E2E y contract testing
│   ├── ci-cd-pipelines.md         # Pipeline de integración y despliegue continuo con control de calidad
│   └── static-analysis-sonarqube.md # Deuda técnica, cobertura de código y linters
└── 05-case-studies-templates/     # Portafolio de gestión aplicable
    ├── post-mortem-template.md    # Plantilla para analizar fallos en producción (Blameless)
    └── agile-project-blueprint.md  # Caso práctico: estimaciones, WBS y riesgos aplicados
```

---

## Pilares del Manifiesto de Calidad

1. **Enfoque Centrado en el Valor**: Cada línea de código, tarea de planificación o historia de usuario debe aportar un valor medible al negocio y al cliente.
2. **Calidad Integrada (Built-in Quality)**: La calidad no es una fase final; es una disciplina diaria de diseño, pruebas automatizadas y refactorización constante.
3. **Mejora Continua e Inspección**: Analizar métricas reales (tiempos de ciclo, cobertura, fallas) para adaptar de manera iterativa los procesos y herramientas.
4. **Cultura de Responsabilidad Compartida**: Desarrolladores, Product Owners, Scrum Masters y Stakeholders cooperan de manera transparente para alcanzar objetivos comunes.
