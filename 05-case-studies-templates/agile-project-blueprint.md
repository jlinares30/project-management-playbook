# Caso Práctico: Blueprint de Gestión Ágil de Proyectos

Este caso práctico simula el ciclo de vida completo de planificación y ejecución ágil de un proyecto de software ficticio: **"PayFlow Lite"**, una API de micropagos para creadores de contenido.

---

## 1. Ficha del Proyecto y Objetivos

* **Nombre del Proyecto**: PayFlow Lite
* **Sponsor / Cliente**: VP de Producto de la Unidad de Negocio de Creadores
* **Objetivo de Negocio**: Permitir que creadores de contenido reciban micropagos (de $0.10 a $5.00 USD) en menos de 5 segundos con una comisión máxima del 1%.
* **Plazo**: 3 meses (6 Sprints de 2 semanas cada uno).

---

## 2. Desglose del Alcance (EDT/WBS Simplificada)

```text
1. PayFlow Lite (Proyecto)
   ├── 1.1 Core Backend (Motor de Pagos)
   │   ├── 1.1.1 API de Recepción y Firma de Transacciones
   │   └── 1.1.2 Bóveda de Tokens y Conciliación Monetaria
   ├── 1.2 Frontend (Dashboard de Creador)
   │   ├── 1.2.1 Componente Web embebible para Propinas
   │   └── 1.2.2 Panel de Control de Saldo y Retiros
   └── 1.3 Calidad e Infraestructura
       ├── 1.3.1 Pipeline de CI/CD con SonarQube
       └── 1.3.2 Pruebas de Carga (1,000 transacciones/segundo)
```

---

## 3. Gestión y Planificación Ágil

### Planificación de la Entrega (Release Plan)

* **Sprint 1 & 2 (MVP Core)**: 
  * Desarrollo del API de pagos (1.1.1) e infraestructura base.
  * *Hito*: Primera transacción simulada procesada con éxito en local.
* **Sprint 3 & 4 (Integración y Vista)**:
  * Creación del panel de control de saldo (1.2.2) e integración con pasarela real en sandbox.
  * *Hito*: Dashboard funcional mostrando saldo simulado acumulado.
* **Sprint 5 & 6 (Validación y Seguridad)**:
  * Pruebas de carga (1.3.2), auditoría de seguridad y despliegue del componente de propinas (1.2.1).
  * *Hito*: Lanzamiento controlado a producción para 50 creadores beta (Closed Beta).

---

## 4. Matriz de Riesgos Inicial del Blueprint

| ID | Riesgo Detectado | Prob. | Imp. | Score | Estrategia de Mitigación |
| :--- | :--- | :---: | :---: | :---: | :--- |
| **R-PF-01** | **Bajo rendimiento en transacciones simultáneas**. | 3 | 5 | **15** (Crítico) | Diseñar el motor de pagos de forma asíncrona mediante colas de mensajería (ej. RabbitMQ o BullMQ). |
| **R-PF-02** | **Fallas en la conciliación bancaria al final del día**. | 2 | 5 | **10** (Mod.) | Implementar un sistema de contabilidad de partida doble inmutable en la base de datos de transacciones. |
| **R-PF-03** | **Retraso en la verificación de identidad (KYC)**. | 4 | 3 | **12** (Mod.) | Utilizar un proveedor de KYC SaaS con integración out-of-the-box (ej. Stripe Identity) en lugar de construirlo in-house. |

---

## 5. Ejemplo de Criterios de Aceptación (User Story en Gherkin)

**Historia de Usuario**: Registro de Retiro de Fondos  
> **Como** creador registrado con saldo acumulado  
> **Quiero** solicitar la transferencia de mis ganancias a mi cuenta de banco  
> **Para** disponer del dinero real cobrado  

**Escenario: Solicitud de retiro exitosa**
```gherkin
Given (Dado) que el creador ha iniciado sesión y tiene un saldo disponible de $150 USD
And (Y) tiene una cuenta bancaria debidamente vinculada y verificada
When (Cuando) solicita un retiro de "$100 USD"
Then (Entonces) el sistema debe descontar "$100 USD" del saldo disponible
And (Y) marcar el saldo como "En tránsito"
And (Y) enviar una solicitud de transferencia a la pasarela bancaria
And (Y) mostrar un mensaje de éxito: "Tu solicitud de retiro por $100 USD está siendo procesada"
```
