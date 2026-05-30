# Métricas Ágiles: Midiendo el Éxito y la Predecibilidad

Las métricas ágiles no se utilizan para castigar o juzgar el desempeño individual, sino para diagnosticar la salud del flujo de trabajo, mejorar las estimaciones y predecir entregas futuras de forma realista.

---

## Lead Time vs. Cycle Time

Estas son las dos métricas fundamentales para medir la eficiencia del flujo de trabajo, especialmente populares en Kanban y Lean.

```text
|<--------------------------- Lead Time --------------------------->|
|                                                                   |
+--------------------+---------------------+------------------------+
|  Backlog (Idea)    |   En Desarrollo     |  Desplegado en Prod.   |
+--------------------+---------------------+------------------------+
                     |                                              |
                     |<------------ Cycle Time ------------>|
```

* **Lead Time (Tiempo de Entrega)**:
  * **Definición**: El tiempo total transcurrido desde que una solicitud o requerimiento entra en el backlog hasta que se entrega en producción al usuario final.
  * **Objetivo**: Reducirlo al mínimo para acortar el bucle de feedback del cliente.
* **Cycle Time (Tiempo de Ciclo)**:
  * **Definición**: El tiempo transcurrido desde que el equipo de desarrollo comienza activamente a trabajar en un ítem (cambia a estado *En progreso*) hasta que se completa y está listo para ser entregado.
  * **Objetivo**: Lograr que sea predecible y consistente, reduciendo la variabilidad del proceso.

---

## Velocity (Velocidad en Scrum)

* **Definición**: La cantidad de esfuerzo (generalmente medido en Puntos de Historia o cantidad de tareas) que un equipo Scrum completa en un Sprint promedio.
* **Uso correcto**:
  * **Predecibilidad**: Ayuda al PO a proyectar cuántos Sprints se necesitarán para completar el alcance del Product Backlog.
  * **Estabilidad**: Permite al equipo no comprometerse de más durante la planificación de un Sprint.
* **Antipatrón común**: Comparar la velocidad entre equipos diferentes. Los puntos de historia son estimaciones relativas específicas de cada equipo.

---

## Gráficos de Flujo y Progreso

### 1. Burn-down Chart (Gráfico de Trabajo Pendiente)
Muestra el trabajo restante en un Sprint día a día. Ayuda al equipo a detectar rápidamente si está en riesgo de no cumplir con la meta del Sprint.
* **Línea ideal**: Trayectoria diagonal descendente desde el inicio hasta el fin del Sprint.
* **Línea real**: Representa el estado diario. Desviaciones prolongadas por encima de la línea ideal indican un alcance muy grande o impedimentos no resueltos.

### 2. Burn-up Chart (Gráfico de Trabajo Completado)
Muestra el trabajo completado en comparación con el alcance total a lo largo del tiempo. Es ideal para gestionar lanzamientos de proyectos de mediano plazo.
* **Línea superior**: Muestra el alcance total del proyecto (permite rastrear gráficamente el *scope creep* o cambios en el alcance).
* **Línea inferior**: Muestra el total de puntos completados acumulados.

### 3. CFD (Diagrama de Flujo Acumulado)
Muestra la cantidad de tareas en cada estado del tablero Kanban a lo largo del tiempo.
* **Bandas paralelas**: Indican un flujo de trabajo estable y saludable.
* **Banda ensanchándose (WIP grande)**: Alerta de un cuello de botella en ese estado específico (ej. muchas tareas acumuladas en QA esperando revisión).
