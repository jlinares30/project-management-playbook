# Valor y Priorización Basada en Valor

> [!NOTE]
> **Enfoque de Ingeniería y Liderazgo Técnico (Big Tech Mindset)**  
> Un backlog no se ordena por "lo que pide quien grita más fuerte", sino por el valor que cada ítem aporta frente a lo que cuesta construirlo. Antes de estimar o planificar, un líder técnico debe poder responder: *¿qué tipo de valor genera esta funcionalidad y para quién?* Si no hay respuesta, el ítem probablemente no debería construirse.

---

## ¿Qué es el Valor?

El valor es el motivo por el que existe el proyecto. Una actividad genera valor cuando:

* Produce algo útil para el cliente o la organización.
* Se traduce en beneficios económicos.
* Genera satisfacción y motivación en las personas.
* Cuida la salud y el bienestar del equipo (un ritmo insostenible destruye valor a mediano plazo).

### Perspectivas del Valor

Cada parte interesada percibe el valor de forma distinta, por lo que conviene explicitar desde qué perspectiva se está priorizando:

| Perspectiva | ¿Quién la representa? | ¿Qué busca? |
| :--- | :--- | :--- |
| **Valor para la organización** | Patrocinador y accionistas. | Retorno de la inversión (ROI), logro de la estrategia, resultados o mejoras medibles. |
| **Valor para el cliente** | Cliente y usuarios finales. | Productos, servicios y requisitos resueltos; poder usar las funciones que necesita. |
| **Valor social** | Comunidades y entorno. | Contribución a grupos de personas, a la comunidad o al medio ambiente. |

### Entregable, Resultado y Valor

El PMBOK 7 separa el **entregable** del **resultado** que ese entregable produce en la organización. Las antiguas "áreas de conocimiento" se integraban para producir un entregable; los actuales "dominios de desempeño" se enfocan en el resultado.

```text
[Procesos, métodos, artefactos] ──> [ENTREGABLE] ──> [RESULTADO] ──> [VALOR]
                                     (output)         (outcome)       (beneficio)
```

El valor es una **consecuencia** del entregable, no el entregable en sí: desplegar un módulo de pagos es el entregable; que los clientes paguen sin fricción es el resultado; el aumento de ingresos es el valor.

---

## Las 4 Categorías de Valor Comercial

Toda funcionalidad debería poder clasificarse en al menos una de estas categorías. Si no encaja claramente en ninguna, es una señal de que aporta poco valor de negocio real.

| Categoría | Qué significa | Ejemplos en software |
| :--- | :--- | :--- |
| **1. Aumentar ingresos** | Ganar mercado, mejorar el valor percibido por el cliente o habilitar valor futuro (I+D). | Funcionalidad premium en un SaaS, integración con pasarelas de pago, app móvil para nuevos mercados, recomendaciones personalizadas con ML. |
| **2. Proteger ingresos** | Evitar la pérdida de clientes o ingresos ya existentes. | Pruebas automatizadas que reducen fallos en producción, backups y redundancia en la nube, seguridad (cifrado, 2FA), monitoreo de UX para proteger la retención. |
| **3. Evitar costos** | Cumplir obligaciones legales, ambientales y sociales para no incurrir en multas, penalidades o demandas. | Cumplimiento de GDPR / leyes de protección de datos, auditorías de seguridad, uso correcto de licencias open-source. |
| **4. Reducir costos** | Mejorar la eficiencia y el desempeño para disminuir costos operativos futuros. | Automatización de procesos, mejora de herramientas internas, inversión en el equipo y su calidad de vida laboral. |

---

## Técnicas de Priorización Basada en Valor

Una vez priorizado el Product Backlog queda claro el Release Plan: qué releases van primero y cuál es el MVP.

### 1. MoSCoW (valor para el cliente)

Divide los requisitos en cuatro categorías, de mayor a menor prioridad:

| Categoría | Significado | Criterio |
| :--- | :--- | :--- |
| **Must** (debe) | Imprescindible. | Sin esto el producto carece de valor. Forma parte del MVP. |
| **Should** (debería) | Alto valor, no imprescindible. | Sin esto el producto funciona, pero queda austero. |
| **Could** (podría) | Deseable. | Se hace solo si el tiempo y los recursos lo permiten. |
| **Won't** (no por ahora) | Poco aporte de valor. | No se aborda a corto plazo; puede reconsiderarse en el futuro. |

**Ejemplo (la hamburguesa):** *Must* = pan y carne; *Should* = queso y lechuga; *Could* = tocino y salsas especiales; *Won't* = pan artesanal de masa madre.

### 2. Valor vs. Costo (enfoque ROI)

No solo considera el valor de negocio del requisito, sino también el costo de construirlo. Es la misma idea que el indicador financiero ROI: beneficio obtenido frente a inversión realizada.

```text
  Valor
   Alto │  HACER PRIMERO        │  PLANIFICAR
        │  (alto valor,         │  (alto valor,
        │   bajo costo)         │   alto costo)
        ├───────────────────────┼──────────────────────
   Bajo │  RELLENO              │  DESCARTAR
        │  (bajo valor,         │  (bajo valor,
        │   bajo costo)         │   alto costo)
        └───────────────────────┴──────────────────────
              Costo Bajo               Costo Alto
```

### 3. WSJF (Weighted Shortest Job First)

Modelo de SAFe que divide el costo de la demora (valor + urgencia + reducción de riesgo/oportunidad) entre el esfuerzo. La fórmula y un ejemplo numérico completo están en [Agile Portfolio Management](../02-project-planning/agile-portfolio-management.md); se aplica igual a nivel de backlog de producto.

### ¿Cuál usar?

| Técnica | Considera el costo | Mejor para |
| :--- | :--- | :--- |
| **MoSCoW** | No (solo valor para el cliente). | Delimitar rápidamente el MVP con stakeholders no técnicos. |
| **Valor vs. Costo** | Sí (cualitativo). | Ordenar un backlog cuando ya existen estimaciones de esfuerzo. |
| **WSJF** | Sí (cuantitativo, añade urgencia y riesgo). | Comparar iniciativas grandes que compiten por la misma capacidad. |

---

## Caso Práctico: Del Valor al MVP en Tres Pasos

Flujo recomendado para definir el alcance de un MVP con el equipo:

1. **Clasificar por valor:** listar las funcionalidades candidatas y marcar a cuál de las 4 categorías de valor comercial pertenece cada una.
2. **Estimar el esfuerzo:** asignar puntos con la secuencia de Fibonacci mediante [Planning Poker](agile-schedule-management.md#planning-poker).
3. **Priorizar con MoSCoW:** con valor y esfuerzo a la vista, clasificar cada funcionalidad. Las que queden en *Must* son, por definición, el MVP.

| Funcionalidad | Categoría de valor | Esfuerzo | MoSCoW |
| :--- | :--- | :---: | :---: |
| Registro e inicio de sesión | Proteger ingresos | 3 | Must |
| Pago con tarjeta | Aumentar ingresos | 8 | Must |
| Consentimiento de datos personales | Evitar costos | 2 | Must |
| Panel de reportes para administradores | Reducir costos | 5 | Should |
| Recomendaciones personalizadas | Aumentar ingresos | 13 | Could |
| Modo oscuro | *(no encaja claramente)* | 3 | Won't |
