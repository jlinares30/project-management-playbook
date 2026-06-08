# Compendio e Implementación de Normas ISO en Ingeniería de Software

Este compendio centraliza, explica y ejemplifica las normas ISO clave mencionadas a lo largo de este playbook. El objetivo es proporcionar una referencia rápida, comprensible y orientada a la práctica real en proyectos de software.

---

## Índice de Normas Explicadas
1. [ISO 9001: Gestión de Calidad Organizativa](#1-iso-9001-gestión-de-la-calidad-organizativa)
2. [ISO/IEC 12207: Procesos del Ciclo de Vida del Software](#2-iso-iec-12207-procesos-del-ciclo-de-vida-del-software)
3. [ISO/IEC 25010: Modelo de Calidad del Producto de Software](#3-iso-iec-25010-modelo-de-calidad-del-producto-de-software)
4. [ISO/IEC 27001 y 27002: Seguridad de la Información (SGSI)](#4-iso-iec-27001-y-27002-seguridad-de-la-información-sgsi)
5. [ISO/IEC 15504 SPICE / ISO 330xx: Capacidad y Madurez de Procesos](#5-iso-iec-15504-spice--isoiec-330xx-capacidad-y-madurez-de-procesos)
6. [ISO/IEC 29110: Ciclo de Vida del Software para PYMEs](#6-iso-iec-29110-ciclo-de-vida-del-software-para-pequeñas-organizaciones-pymes)
7. [ISO/IEC 14764: Mantenimiento del Software](#7-iso-iec-14764-mantenimiento-de-software)
8. [ISO/IEC 15939: Proceso de Medición de Software](#8-iso-iec-15939-proceso-de-medición-de-software)
9. [Estándares Organizacionales: ISO 21500, ISO 30401 e ISO 56002](#9-estándares-organizacionales-auxiliares)

---

## 1. ISO 9001: Gestión de la Calidad Organizativa

* **¿Qué es?** El estándar global para diseñar e implementar un **Sistema de Gestión de la Calidad (SGC)** en cualquier tipo de organización.
* **Explicación sencilla:** No te dice cómo programar, sino cómo dirigir tu empresa de forma que siempre escuches al cliente, midas tus errores, capacites a tu gente y mejores continuamente tus procesos.
* **Ejemplo práctico:** Una software house define que toda queja de un cliente por fallas en producción debe registrarse en un software de tickets (como Jira Service Management), analizarse en una reunión mensual de mejora, y traducirse en acciones correctivas para que el bug no vuelva a ocurrir.
* **Integración Ágil:** Se alinea directamente con el principio de la **Retrospectiva del Sprint** (inspeccionar y adaptar los procesos del equipo de forma continua).

---

## 2. ISO/IEC 12207: Procesos del Ciclo de Vida del Software

* **¿Qué es?** El marco de referencia oficial que define **qué tareas y procesos** deben realizarse desde que se concibe una idea de software hasta que el sistema se retira del mercado.
* **Explicación sencilla:** Es un catálogo estructurado (30 procesos en la versión 2017) que describe todas las actividades de ingeniería de software (requisitos, diseño, código, pruebas, mantenimiento) y su gobernanza administrativa.
* **Ejemplo práctico:** Al iniciar el desarrollo de una aplicación bancaria, el equipo utiliza el *Proceso de Definición de Requisitos* para escribir historias de usuario detalladas, el *Proceso de Gestión de Configuración* para definir las políticas de ramificación (Git branching strategy) y el *Proceso de Integración* para configurar pipelines automatizados.
* **Integración Ágil:** Traduce los procesos técnicos tradicionales a tareas ágiles diarias: el refinamiento del backlog cubre la definición de requisitos, y las pruebas de aceptación de la demo del sprint cubren los procesos de validación.

---

## 3. ISO/IEC 25010: Modelo de Calidad del Producto de Software

* **¿Qué es?** El estándar para evaluar la **calidad técnica y funcional del código** y del producto entregado mediante 8 características principales.
* **Explicación sencilla:** Es una lista de comprobación técnica que ayuda a responder: ¿Es nuestro software rápido? ¿Es seguro? ¿Es fácil de modificar y mantener? ¿Es compatible con otros sistemas?
* **Ejemplo práctico:** Para garantizar la *Mantenibilidad*, la empresa configura SonarQube para medir el *Índice de Mantenibilidad* y bloquear cualquier Pull Request que contenga métodos con alta complejidad ciclomática o código duplicado. Para la *Fiabilidad*, se configuran servidores en la nube con escalamiento automático (auto-scaling) para asegurar que el sistema no se caiga bajo carga.
* **Integración Ágil:** Define directamente los **Criterios de Aceptación No Funcionales** de las historias de usuario y alimenta la Definition of Done (DoD).

---

## 4. ISO/IEC 27001 y 27002: Seguridad de la Información (SGSI)

* **¿Qué es?** El estándar que define cómo diseñar un **Sistema de Gestión de la Seguridad de la Información (SGSI)** (ISO 27001) y la guía detallada de los controles de seguridad aplicables (ISO 27002).
* **Explicación sencilla:** Es la norma para proteger los datos de tu empresa y clientes garantizando tres cosas (Tríada CIA): que solo entren personas autorizadas (Confidencialidad), que los datos sean correctos y no se alteren (Integridad), y que los servidores estén siempre activos (Disponibilidad).
* **Ejemplo práctico:** Una fintech exige que todos sus desarrolladores usen Autenticación de Doble Factor (2FA) para entrar a GitHub, prohíbe subir credenciales hardcodeadas (usando herramientas como GitGuardian), cifra la base de datos de usuarios en reposo y realiza simulacros mensuales de restauración de copias de seguridad (backups).
* **Integración Ágil:** Alimenta el pipeline de DevSecOps con análisis automatizados de seguridad (SAST/DAST) y auditorías en cada compilación (Daily Builds).

---

## 5. ISO/IEC 15504 (SPICE) / ISO/IEC 330xx: Capacidad y Madurez de Procesos

* **¿Qué es?** El modelo utilizado para evaluar el **nivel de madurez** y capacidad de los procesos de software dentro de una empresa en una escala del 0 al 5.
* **Explicación sencilla:** Sirve como termómetro para medir qué tan organizada es tu empresa: si trabaja de forma caótica (Nivel 0), si los proyectos son individuales y reactivos (Nivel 1), si hay procesos estandarizados corporativos (Nivel 3), o si se optimizan usando datos cuantitativos (Niveles 4 y 5).
* **Ejemplo práctico:** Una empresa evalúa su proceso de testing. Descubre que cada programador prueba "como quiere" (Nivel 1). Deciden formalizar una política de testing e implementar una herramienta corporativa estándar de automatización de pruebas para toda la organización, subiendo así al Nivel 3 (Establecido).
* **Integración Ágil:** Permite que las organizaciones midan la madurez de su transformación ágil de forma cuantitativa, asegurando que la agilidad no se limite a reuniones de Scrum sino que sea un proceso predecible y optimizado.

---

## 6. ISO/IEC 29110: Ciclo de Vida del Software para Pequeñas Organizaciones (PYMEs)

* **¿Qué es?** Una versión simplificada de ISO 12207 diseñada específicamente para **pequeñas organizaciones de software** (hasta 25 personas).
* **Explicación sencilla:** Las startups y PYMEs no tienen el dinero ni el personal para implementar los 30 procesos de la ISO 12207. Esta norma resume lo esencial en dos procesos clave: Gestión de Proyectos y Entrega de Software.
* **Ejemplo práctico:** Una startup de 5 desarrolladores adopta la ISO 29110. En lugar de documentar cientos de páginas de arquitectura, utilizan plantillas de 1 página para el Project Charter, definen un flujo sencillo de control de cambios, y unifican su repositorio de código en una sola rama para agilizar despliegues.
* **Integración Ágil:** Ideal para startups que usan Scrum o Kanban y necesitan demostrar formalidad de procesos ante grandes clientes corporativos o licitaciones públicas sin perder agilidad.

---

## 7. ISO/IEC 14764: Mantenimiento de Software

* **¿Qué es?** El estándar que proporciona directrices y clasificaciones para la fase de **mantenimiento del software** tras su puesta en producción.
* **Explicación sencilla:** Clasifica y define las reglas de cómo actuar frente a las modificaciones del sistema una vez que está operativo, dividiéndolo en 4 tipos de mantenimiento:
  1. **Correctivo (Corrective):** Corregir bugs que fallan en producción (ej. solucionar una caída del servidor).
  2. **Preventivo (Preventive):** Modificar el código antes de que falle (ej. refactorizar un bloque de código legacy difícil de entender).
  3. **Adaptativo (Adaptive):** Adaptar el sistema a nuevos entornos (ej. migrar la base de datos de un servidor local a AWS).
  4. **Perfectivo (Perfective):** Añadir nuevas características o mejoras solicitadas por el cliente (ej. añadir un botón de pago con Apple Pay).
* **Ejemplo práctico:** Un equipo de soporte recibe un ticket en el que el botón de registro se queda congelado. Clasifican la tarea como *Mantenimiento Correctivo*, programan el parche, realizan pruebas de regresión automáticas para validar que no afecte otras secciones, y despliegan la corrección.
* **Integración Ágil:** Ayuda a los Product Owners a priorizar y categorizar el Sprint Backlog entre historias de usuario nuevas (Perfectivo/Adaptativo), refactorizaciones (Preventivo) y resolución de bugs (Correctivo).

---

## 8. ISO/IEC 15939: Proceso de Medición de Software

* **¿Qué es?** El estándar que define las actividades y tareas necesarias para planificar, recopilar, analizar y reportar **métricas en proyectos de software**.
* **Explicación sencilla:** Te ayuda a definir qué vas a medir, cómo vas a recopilar el dato de forma objetiva, y cómo usar esos gráficos para tomar decisiones ejecutivas en lugar de suposiciones.
* **Ejemplo práctico:** Un departamento de ingeniería quiere medir la calidad de sus entregas. Define la métrica *Densidad de Defectos* (número de bugs detectados en QA por cada 100 puntos de historia). El pipeline de CI recopila automáticamente el dato en cada sprint y genera un tablero de control en Grafana para el CTO.
* **Integración Ágil:** Proporciona el marco analítico para métricas como la *Velocidad del Equipo*, *Cycle Time*, *Lead Time* y el *Burn-down chart*, asegurando que la toma de decisiones del equipo esté fundamentada en datos duros.

---

## 9. Estándares Organizacionales Auxiliares

### A. ISO 21500 (Gobernanza y Gestión de Proyectos)
* **¿Qué es?** Directrices y conceptos de alto nivel para gestionar proyectos de manera estructurada en la organización.
* **Aplicación:** Sirve para unificar el lenguaje y los procesos de gestión entre la Oficina de Proyectos (PMO) tradicional y los equipos que operan con marcos ágiles (Scrum/Kanban).

### B. ISO 30401 (Sistemas de Gestión del Conocimiento)
* **¿Qué es?** Requisitos para establecer sistemas y cultura que fomenten la creación, retención e intercambio del conocimiento organizacional.
* **Aplicación:** En software, esto se traduce en eliminar silos de conocimiento mediante la documentación estructurada de arquitecturas (ej. en Confluence), y la realización sistemática de capacitaciones internas (Brown Bag Sessions) y pair programming.

### C. ISO 56002 (Gestión de la Innovación)
* **¿Qué es?** Guía para establecer y mantener un sistema de gestión de la innovación para responder rápidamente a los cambios del mercado.
* **Aplicación:** Fomenta la creación de células de innovación técnica en la empresa (ej. organizar Hackathons trimestrales, dar tiempo dedicado de investigación a desarrolladores) para construir prototipos rápidos y probar nuevas tecnologías sin interrumpir el flujo del negocio core.
