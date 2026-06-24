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
│   ├── agile-culture-fundamentals.md # Fundamentos ágiles, cultura y roles
│   ├── scrum-and-kanban.md        # Roles, ceremonias y cuándo usar cada flujo
│   ├── user-stories-discovery.md  # Criterios de aceptación (Gherkin/BDD) y Story Mapping
│   ├── agile-metrics.md           # Velocity, Lead Time, Cycle Time y Burn-down charts
│   └── agile-schedule-management.md # Release Plan, precedencias y dependencias de cronograma
├── 02-project-planning/           # Gestión del Alcance y Gobernanza
│   ├── agile-integration-management.md # Project Charter ágil, planes híbridos y lecciones
│   ├── scope-and-wbs.md           # Estructura de Desglose de Trabajo (EDT/WBS) y MVP
│   ├── agile-cost-management.md   # Estimación Top-down, capacity-based pricing y Agile EVM
│   ├── agile-resource-management.md # Células multifuncionales y Servant Leadership
│   ├── roles-and-glossary.md      # Comparación de roles (PMBOK vs Agile) y glosario cruzado
│   ├── risk-management.md         # Matriz de riesgos (Mitigación de fallas en proyectos)
│   ├── stakeholders-comm.md       # Gestión de expectativas y reportes de estado
│   └── agile-procurement-management.md # Gestión de adquisiciones y contratos ágiles
├── 03-software-quality-standards/ # Estándares y Gobernanza Técnica
│   ├── quality-fundamentals-gurus.md # Teoría de calidad, Garvin, gurús, costos y curva de IBM
│   ├── iso-iec-12207.md           # Estándar oficial ISO/IEC 12207:2017 (30 procesos y 4 grupos)
│   ├── quality-models-iso-25010.md# Atributos de calidad (Mantenibilidad, Seguridad, Eficiencia)
│   ├── agile-quality-management.md # QA vs QC, testing en la iteración (daily builds, regression)
│   ├── process-modeling-bpmn.md   # Modelado de procesos, SIPOC y notación BPMN 2.0 (Bizagi)
│   ├── information-security-iso27001.md # Tríada CIA, SGSI y controles de seguridad (ISO 27001/27002)
│   ├── process-capability-maturity.md # Modelo de capacidad y madurez de procesos (ISO 15504 SPICE)
│   └── iso-standards-compendium.md # Compendio de normas ISO (9001, 12207, 25010, 27001, etc.)
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
