# Modelo de Evaluación de Madurez y Capacidad de Procesos (ISO/IEC 15504 / ISO/IEC 33000)

> [!NOTE]
> **Evaluación y Habilitación Organizacional**
> Para que una organización de software mejore continuamente, debe evaluar de forma objetiva la capacidad de sus procesos actuales. El estándar **ISO/IEC 15504** (también conocido como **SPICE**) y su evolución **ISO/IEC 33000** proporcionan un modelo bidimensional para evaluar la madurez de los procesos y la capacidad de la organización.

---

## 1. Niveles de Madurez de Capacidad de Procesos y Marcos Recomendados

A continuación se detalla la escala de madurez (niveles del 0 al 5) según el estándar de capacidad, junto con las recomendaciones y marcos de referencia (normas ISO, metodologías ágiles y guías de gestión) asociados a cada nivel para habilitar su cumplimiento:

| Nivel | Descripción | Descripción de Capacidad | Marcos y Estándares Recomendados (Rec.) |
| :---: | :--- | :--- | :--- |
| **0** | **INCOMPLETO**<br>*(Incomplete)* | El proceso no se implementa o no logra cumplir con su propósito establecido. Existe poca o ninguna sistematización. | • Directivas organizacionales básicas.<br>• Procedimientos informales no estandarizados. |
| **1** | **REALIZADO**<br>*(Performed)* | El proceso logra cumplir con su propósito, pero de manera reactiva e individualizada por proyecto. | • **[ISO/IEC 12207](iso-iec-12207.md):** Procesos base de ciclo de vida ejecutados de forma técnica. |
| **2** | **GESTIONADO**<br>*(Managed)* | El proceso se planifica, supervisa y ajusta de forma sistemática. Los entregables se establecen y controlan de acuerdo a planes. | • **[PMBOK® / Scrum](01-agile-frameworks/scrum-and-kanban.md):** Marcos de gestión y roles definidos.<br>• **ISO 21500:** Directrices para la gestión de proyectos.<br>• **Ciclo PDCA/PECA:** Mejora iterativa a nivel operativo. |
| **3** | **ESTABLECIDO**<br>*(Established)* | El proceso gestionado se implementa utilizando un proceso estándar definido y documentado a nivel de toda la organización. | • **[ISO/IEC 25010](quality-models-iso-25010.md):** Modelos formales de calidad de producto.<br>• **ISO 9001:** Enfoque sistemático en la Gestión de la Calidad (Q) organizativa. |
| **4** | **PREDECIBLE**<br>*(Predictable)* | El proceso establecido opera de manera estable dentro de límites definidos cuantitativamente para lograr sus resultados. | • **[ISO/IEC 27001 / 27002](information-security-iso27001.md):** Seguridad de la información integrada.<br>• **[ISO/IEC 12207](iso-iec-12207.md):** Procesos maduros del ciclo de vida.<br>• **[ISO/IEC 25010](quality-models-iso-25010.md):** Atributos de calidad medidos cuantitativamente.<br>• **ISO/IEC 90003:** Directrices de aplicación de ISO 9001 en desarrollo de software.<br>• **ISO 21500:** Gobernanza estructurada de proyectos. |
| **5** | **OPTIMIZADO**<br>*(Optimizing)* | El proceso se mejora continuamente para cumplir con los objetivos comerciales actuales y futuros de la organización. | • **Marcos Integrados:** Coexistencia de ISO 25010, ISO 9001, ISO 21500 e ISO 12207.<br>• **ISO 56000 / 56002:** Sistemas de Gestión de la Innovación.<br>• **ISO 30401:** Sistemas de Gestión del Conocimiento. |

---

## 2. Relación de los Estándares en el Ciclo de Madurez

El modelo de madurez actúa como una hoja de ruta evolutiva para la ingeniería y gobernanza del software:

```mermaid
graph TD
    L0[Nivel 0: Incompleto - Directivas] --> L1[Nivel 1: Realizado - ISO 12207]
    L1 --> L2[Nivel 2: Gestionado - Scrum / PMBOK / ISO 21500 / PDCA]
    L2 --> L3[Nivel 3: Establecido - ISO 25010 / ISO 9001]
    L3 --> L4[Nivel 4: Predecible - ISO 27001 / ISO 90003]
    L4 --> L5[Nivel 5: Optimizado - Innovación ISO 56000 / Conocimiento ISO 30401]
```

* **Transición del Caos a la Agilidad (Nivel 0 al Nivel 2):** Se implementan marcos ágiles (Scrum, Kanban) y el ciclo PECA para estructurar y gestionar el trabajo diario antes de buscar certificaciones de procesos complejos.
* **Institucionalización (Nivel 3):** Las buenas prácticas se expanden a toda la compañía. Se formalizan los modelos de calidad del producto (ISO 25010) y se unifica la calidad organizativa (ISO 9001).
* **Control Cuantitativo e Innovación (Nivel 4 al Nivel 5):** Se integran la seguridad robusta (ISO 27001), la gobernanza de conocimiento (ISO 30401) y la gestión sistemática de la innovación (ISO 56000) para garantizar que la mejora sea continua y el negocio permanezca a la vanguardia.
