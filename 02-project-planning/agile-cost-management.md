# Gestión de Costos en Proyectos Ágiles

> [!NOTE]
> **Enfoque de Ingeniería y Liderazgo Técnico (Big Tech Mindset)**  
> En Big Tech, las estimaciones detalladas del costo de infraestructura y mano de obra a nivel de micro-tareas antes de empezar el desarrollo han demostrado ser ineficaces. Se adopta la estimación "Top-Down" y la estabilización de costos mediante el financiamiento de equipos de ingeniería fijos y estables (*capacity-based funding*), gestionando el retorno de inversión (ROI) a través de la priorización constante del Product Backlog.

---

## Planificación Financiera: Tradicional vs. Ágil

En los proyectos predictivos clásicos, el presupuesto se calcula sumando el costo estimado de cada tarea individual detallada en el cronograma. En Agile, el presupuesto total está predefinido de antemano y es fijo.

### Características del Enfoque Ágil
* **Equipos Dedicados como Costo Fijo:** Dado que el mayor gasto de un proyecto de software es la mano de obra, y el tamaño del equipo es estable y dedicado, el costo por iteración (Sprint) es sumamente predecible e invariable:
  $$\text{Costo del Sprint} = \text{Costo total de miembros del equipo} \times \text{Duración del Sprint}$$
* **Presupuesto Total:**
  $$\text{Presupuesto Proyectado} = \text{Costo del Sprint} \times \text{Número de Sprints del Release Plan}$$
* **Trade-off del Presupuesto Fijo:** Al agotarse el dinero o el tiempo presupuestado, el proyecto finaliza. Si quedaron historias sin hacer en el Product Backlog, estas quedan excluidas de la entrega. Sin embargo, gracias al enfoque adaptativo de priorización, las tareas que no se construyeron son siempre las de **menor valor de negocio**.

---

## Métodos de Estimación: De Arriba hacia Abajo (Top-Down)

En el desarrollo de software es imposible predecir de forma precisa cada tarea técnica y dependencia con meses de antelación. Por ello, Agile utiliza la estimación **Top-Down (De arriba hacia abajo)**:

```text
  TRADICIONAL (Bottom-Up):
  [Estimar Sub-tareas] ──> [Sumar Tareas] ──> [Agregar Paquetes WBS] ──> [Presupuesto Final]
  * Alta fragilidad ante imprevistos técnicos.

  ÁGIL (Top-Down):
  [Presupuesto Límite / Capacidad de Equipo] ──> [Release Plan en Sprints] ──> [Iteración / Valor]
  * Alta tolerancia y adaptabilidad; foco en maximizar el valor entregado por cada dólar invertido.
```

---

## Control de Rendimiento: Agile EVM (Earned Value Management)

El **EVM (Gestión del Valor Ganado)** es una técnica tradicional adaptada a entornos ágiles para comparar el plan original frente al trabajo real completado.

* **Fórmula Ágil:** En lugar de medir horas o dinero consumido para determinar el progreso, Agile EVM mide **Puntos de Historia de Usuario completados** en relación con el Release Plan original.
* **Métricas clave:**
  * **PV (Planned Value / Valor Planificado):** Los puntos de historia que el equipo planificó completar a una fecha determinada.
  * **EV (Earned Value / Valor Ganado):** Los puntos de historia de tareas *realmente terminadas* (que cumplen el Definition of Done) en esa misma fecha.
  * **AC (Actual Cost / Costo Real):** El costo real consumido (ej. salarios del equipo y recursos cloud consumidos durante las iteraciones ejecutadas).
* **SPI (Schedule Performance Index) en Agile:**
  $$\text{SPI} = \frac{\text{EV (Puntos Completados)}}{\text{PV (Puntos Planificados)}}$$
  * Si $\text{SPI} > 1$, el equipo va más rápido de lo planificado.

---

> [!TIP]
> **Pregunta de Entrevista de Big Tech (Engineering Management / TPM)**  
> *Estamos a la mitad de un proyecto con presupuesto fijo y fecha límite inamovible de 3 meses. El Agile EVM muestra un SPI de 0.80. El patrocinador financiero está preocupado por el rendimiento y propone inyectar dos desarrolladores adicionales de forma inmediata para recuperar el cronograma. ¿Cómo responderías como Engineering Manager?*
> 
> **Respuesta Estratégica:**  
> 1. **Invocar la Ley de Brooks (Brooks' Law):** Explicaría al patrocinador que añadir más personas a un proyecto de software retrasado suele retrasarlo aún más a corto plazo (*"Adding manpower to a late software project makes it later"*). La curva de ramp-up (onboarding técnico, configuración de entornos, mentoría por parte de los desarrolladores actuales) restará capacidad neta al equipo durante los próximos 1 o 2 Sprints.
> 2. **Analizar la causa raíz con métricas:** Evalúo si el SPI de 0.80 se debe a dependencias externas bloqueantes, deuda técnica o sobreestimación inicial.
> 3. **Mitigar mediante control del alcance (Scope Trimming):** Propongo mantener el presupuesto y equipo estable para estabilizar la predecibilidad. Dado que el presupuesto es fijo, colaboro con el Product Owner para recortar el 20% de las funcionalidades del final del backlog (las de menor prioridad) para garantizar que el MVP funcional y escalable se entregue a tiempo y dentro del presupuesto inamovible.
