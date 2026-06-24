# Gestión de Adquisiciones en Proyectos Ágiles (Agile Procurement Management)

La gestión de adquisiciones (Procurement) abarca todos los procesos necesarios para comprar o adquirir los productos, servicios o resultados requeridos fuera del equipo de proyecto. En entornos ágiles, este proceso cambia el enfoque tradicional de confrontación contractual por un modelo basado en la colaboración, flexibilidad y entrega continua de valor.

---

## El Enfoque de Adquisición: Tradicional vs. Ágil

| Característica | Enfoque Predictivo (Tradicional) | Enfoque Adaptativo (Ágil) |
| :--- | :--- | :--- |
| **Alcance y Requisitos** | Cerrados, fijos y detallados exhaustivamente desde el inicio. | Evolutivos, flexibles y priorizados según el valor de negocio. |
| **Relación Contractual** | Formal, defensiva, basada en penalidades y en el cumplimiento estricto de cláusulas. | Colaborativa, transparente, compartiendo riesgos y beneficios. |
| **Adaptabilidad** | El cambio es costoso y requiere un proceso formal de control de cambios. | El cambio se acepta de manera natural al finalizar cada iteración. |
| **Foco del Contrato** | Asegurar la entrega del plan inicial dentro del costo pactado (*Fixed Price*). | Permitir la iteración, el cambio y la co-creación de valor continuo. |

---

## Tipos Comunes de Adquisiciones en Software y TI

En proyectos de tecnología, las adquisiciones se dividen típicamente en:
1. **Contratación de Especialistas:** Incorporación temporal de perfiles especializados no disponibles en el equipo principal (ej. ingenieros de QA, especialistas DevOps, diseñadores UI/UX).
2. **Plataformas y Licencias (SaaS/IaaS/PaaS):** Adquisición de servicios en la nube (AWS, Azure, GCP), pasarelas de pago (Stripe, Paypal) o herramientas SaaS.
3. **Hardware y Equipos Físicos:** Servidores locales, dispositivos móviles de prueba, laptops para desarrollo.
4. **Servicios de Soporte y Mantenimiento:** Contratos de soporte técnico de terceros, capacitación técnica o consultorías.

---

## Principios Ágiles Aplicados a Procurement

1. **Colaboración por encima de la negociación contractual:** El proveedor es visto como un socio estratégico del negocio, no como un mero ejecutor de tareas.
2. **Valor temprano y continuo para el cliente:** Las adquisiciones se estructuran para que el proveedor empiece a entregar código o valor funcional desde los primeros sprints.
3. **Flexibilidad ante el cambio:** El contrato debe permitir pivotar la dirección del desarrollo sin incurrir en penalidades contractuales excesivas.

---

## Tipos de Contratos en Proyectos Ágiles

Los contratos ágiles deben reflejar la flexibilidad del manifiesto ágil. A continuación, se detallan los cuatro modelos de contratación clave (representados visualmente en el diagrama de contratos):

![Tipos de Contratos en Proyectos Ágiles](../week-11.png)

### 1. T&M con Límite (Time & Materials con techo)
* **Descripción:** Se paga al proveedor por las horas de trabajo y los materiales reales consumidos, pero se establece un presupuesto máximo inamovible (*Not-to-Exceed* o *Cap*) que protege al cliente del sobrecosto.
* **Ventajas (+):**
  * Alta flexibilidad ante cambios de alcance.
  * Pago justo basado en el esfuerzo real ejecutado.
* **Desventajas (-):**
  * Requiere un control y auditoría muy rigurosa del gasto y las horas reportadas.
* **Ejemplo Real:** *Toyota Connected* con *VoiceAI Labs*: Contrato T&M con un tope de USD 1.8M para el desarrollo del motor de voz con IA, ajustable por sprint según las prioridades.

### 2. Por Sprint (Contrato por sprint o entregable)
* **Descripción:** La relación comercial y los pagos se estructuran por cada iteración. El proveedor cobra al cerrar con éxito cada sprint o al entregar un incremento funcional validado y aceptado por el Product Owner.
* **Ventajas (+):**
  * Alineación directa con los ciclos ágiles y ceremonias del equipo.
  * Cláusula de salida flexible y sin penalidad al finalizar cualquier sprint.
* **Desventajas (-):**
  * Exige tener criterios de aceptación claros y un *Definition of Done* (DoD) bien definido y compartido.
* **Ejemplo Real:** *Spotify*: Estructura sus acuerdos con proveedores de desarrollo externo mediante entregables y validaciones cada dos semanas por el Product Owner de la respectiva tribu.

### 3. Valor Compartido (Contrato de valor compartido)
* **Descripción:** Cliente y proveedor comparten los beneficios de un resultado exitoso y mitigan de manera conjunta los riesgos de un rendimiento deficiente. Los pagos finales o bonificaciones están ligados a KPIs cuantitativos de negocio acordados.
* **Ventajas (+):**
  * Alinea por completo los incentivos económicos de ambas partes.
  * Fomenta la máxima co-creación de valor y calidad.
* **Desventajas (-):**
  * Complejo de estructurar y redactar a nivel legal.
* **Ejemplo Real:** *ING Bank*: Bonificaciones adicionales a proveedores de software ligadas directamente a la mejora del Net Promoter Score (NPS) del cliente final y a la reducción del *time-to-market*.

### 4. Equipo Dedicado (Dedicated Team / Staff Augmentation)
* **Descripción:** El proveedor asigna un squad técnico exclusivo y estable para trabajar en el proyecto del cliente. El cliente realiza un pago mensual fijo por la capacidad del equipo y mantiene el control total del backlog y las prioridades de desarrollo.
* **Ventajas (+):**
  * Máximo control sobre las prioridades del backlog.
  * Equipo cohesionado, familiarizado con el dominio del negocio y de alta productividad.
* **Desventajas (-):**
  * Representa un costo mensual fijo constante, independientemente de la carga de trabajo asignada.
* **Ejemplo Real:** *Mercado Libre*: Contratación de squads externos dedicados en Argentina, Brasil y Colombia para escalar rápidamente las funcionalidades core de la plataforma de *Mercado Pago*.

---

## Colaboración y Ejecución de Procurement Incremental

* **Procurement Incremental:** En lugar de contratar todo el desarrollo de una sola vez con un único proveedor gigante, los proyectos ágiles contratan de forma incremental (por sprints o fases de validación). Esto permite evaluar el rendimiento del proveedor antes de comprometer más presupuesto, evitando el bloqueo innecesario de proveedores (*vendor lock-in*).
* **Gestión de la Relación con Proveedores:** Se basa en la comunicación frecuente, co-creación del valor, empatía y evaluación continua del desempeño técnico y del alineamiento cultural.

### Riesgos Comunes en Adquisiciones Ágiles
* **Proveedores poco familiarizados con Agile:** Proveedores que intentan imponer metodologías de cascada en el desarrollo.
* **Expectativas desalineadas:** Confusión sobre qué constituye un entregable terminado (falta de consenso en el *Definition of Done*).
* **Contratos tradicionales rígidos:** Cláusulas legales que chocan directamente con la flexibilidad de cambiar el alcance durante los sprints.

### Cláusulas Contractuales Ágiles Clave
* **Entregables iterativos y revisables:** Especificar que los entregables se revisan en la *Sprint Review* del cliente.
* **Sprint Review conjunta:** Obligación del proveedor de participar en las demos para recibir feedback inmediato del Product Owner.
* **Incentivos por valor generado:** Bonificaciones por entrega rápida sin defectos.
* **Penalidades por falta de colaboración:** Cláusulas en caso de que el proveedor oculte bloqueantes o no colabore de manera transparente.

---

## Métricas de Éxito en Procurement Ágil

Para evaluar la efectividad de las adquisiciones, se miden los siguientes indicadores:
* **Velocidad de entrega (Delivery Speed):** Ritmo en que el equipo del proveedor completa puntos de historia de usuario útiles.
* **Nivel de satisfacción con el proveedor:** Evaluaciones periódicas subjetivas/cualitativas del Scrum Master y desarrolladores internos.
* **Porcentaje de cambios aceptados sin impacto negativo:** Capacidad del proveedor de adaptar el código a nuevos requerimientos sin romper funcionalidades existentes ni generar sobrecostos exagerados.
* **Alineación continua con la visión del producto:** Medir si el trabajo del proveedor realmente aporta al ROI del producto.

---

## Caso Práctico: Diseño de Contrato Ágil para Desarrollo Externo

### Contexto del Escenario:
Un equipo ágil necesita contratar temporalmente a una agencia externa para desarrollar un módulo crítico de alta complejidad (por ejemplo, un sistema de recomendación basado en IA). Se anticipa que los requisitos y algoritmos cambiarán cada dos semanas a medida que el Product Owner evalúe los resultados y el feedback de los usuarios en producción.

### Diseño de la Propuesta Contractual:

Para garantizar una entrega continua de valor y evitar los riesgos de sobrecostos o lock-in contractual, se propone estructurar la adquisición bajo el siguiente esquema:

1. **Modalidad Contractual Recomendada:** **Contrato Por Sprint** combinado con un **Tope Máximo (T&M con techo)** para la primera fase de 3 meses.
2. **Sustento de la Modalidad:** 
   * Dado que el alcance del módulo de IA cambiará dinámicamente cada dos semanas según el Product Owner, un contrato por precio fijo tradicional causaría constantes fricciones y renegociaciones de contratos.
   * La estructura de pago por sprint permite al PO redefinir y priorizar el backlog al inicio de cada sprint de forma libre.
   * Si la agencia externa no cumple con el rendimiento esperado o la calidad del código, el cliente puede rescindir el contrato al finalizar el sprint activo sin penalizaciones adicionales.
3. **Criterios de Éxito y Aceptación:**
   * Las historias de usuario de la agencia externa deben cumplir estrictamente con el **Definition of Done (DoD)** del equipo principal (incluyendo pruebas automatizadas y cobertura mínima del 80%).
   * La agencia debe participar activamente en la *Sprint Planning* y la *Sprint Review* conjunta para demostrar el valor ganado directo.
