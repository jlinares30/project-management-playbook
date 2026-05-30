# Descubrimiento de Historias de Usuario

Las historias de usuario son herramientas para fomentar la conversación y la colaboración, no especificaciones estáticas. Este documento detalla cómo definirlas, estimarlas y documentar sus criterios de aceptación con BDD (Behavior-Driven Development).

---

## Criterios INVEST para Buenas Historias de Usuario

Una historia de usuario bien escrita debe cumplir con el acrónimo **INVEST**:

* **I - Independent (Independiente)**: Debe poder desarrollarse, probarse y entregarse sin dependencias directas de otras historias de usuario.
* **N - Negotiable (Negociable)**: No es un contrato cerrado. Invita a la discusión entre el Product Owner y el equipo de desarrollo sobre el alcance exacto.
* **V - Valuable (Valiosa)**: Debe entregar un valor claro y comprensible al usuario final o al negocio.
* **E - Estimable (Estimable)**: El equipo debe entender el alcance lo suficiente para estimar su esfuerzo relativo.
* **S - Small (Pequeña/Apropiada)**: Debe ser lo suficientemente pequeña como para ser completada en un solo Sprint (idealmente de 2 a 5 días).
* **T - Testable (Verificable/Probable)**: Debe tener criterios de aceptación claros que permitan verificar si la implementación funciona correctamente.

---

## Story Mapping: Visualización del Roadmap de Producto

El **Story Mapping** es una técnica de visualización que organiza las historias de usuario según el flujo del usuario (eje horizontal) y la prioridad de entrega / releases (eje vertical).

```text
[Actividad del Usuario] ---------> [Buscar Producto] -----------> [Comprar Producto]
                                         |                             |
[Tareas del Usuario]    ---> [Filtros de búsqueda]     ---> [Pagar con tarjeta]
                                         |                             |
============================= MVP / Release 1 =================================
                         [Búsqueda por texto básico]     [Pago básico con tarjeta]
============================= Release 2 =======================================
                         [Filtro por marca y precio]     [Pago con PayPal]
```

Ayuda a identificar el **MVP (Producto Mínimo Viable)** y a garantizar que el equipo no trabaje en silos, sino en flujos lógicos de extremo a extremo.

---

## Criterios de Aceptación con BDD (Gherkin)

Los criterios de aceptación definen las fronteras de una historia de usuario. Usar el lenguaje Gherkin (BDD) alinea la comprensión del negocio con las pruebas automáticas.

### Estructura Base:
* **Given (Dado)**: El contexto inicial del escenario.
* **When (Cuando)**: La acción que realiza el usuario o el disparador del evento.
* **Then (Entonces)**: El resultado o comportamiento esperado.

### Ejemplo Práctico:

**Historia de Usuario:**
> **Como** cliente registrado  
> **Quiero** aplicar un código de descuento en el carrito de compras  
> **Para** ahorrar dinero en mi pedido final  

**Escenario 1: Aplicación exitosa de un cupón válido**
```gherkin
Given (Dado) que el cliente tiene un carrito de compras con un total de $100
And (Y) existe un cupón de descuento válido "DESCUENTO10" que aplica un 10% de reducción
When (Cuando) el cliente ingresa el cupón "DESCUENTO10" en el campo de descuento
And (Y) presiona el botón "Aplicar"
Then (Entonces) el sistema debe aplicar una reducción de $10 al total
And (Y) mostrar el nuevo total a pagar de $90
And (Y) mostrar un mensaje de éxito: "¡Cupón aplicado correctamente!"
```

**Escenario 2: Intento de aplicación de un cupón expirado**
```gherkin
Given (Dado) que el cliente tiene un carrito de compras activo
And (Y) existe un cupón "EXPIRADO5" cuya fecha de validez ya pasó
When (Cuando) el cliente ingresa el cupón "EXPIRADO5"
And (Y) presiona el botón "Aplicar"
Then (Entonces) el sistema no debe modificar el total del carrito
And (Y) debe mostrar un mensaje de error: "El cupón ingresado ha expirado"
```
