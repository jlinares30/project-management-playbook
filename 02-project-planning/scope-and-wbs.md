# Gestión del Alcance y Estructura de Desglose de Trabajo (EDT/WBS)

> [!NOTE]
> **Enfoque de Ingeniería y Liderazgo Técnico (Big Tech Mindset)**  
> En Big Tech, "alcance" no es una lista de requisitos firmados contractualmente al inicio. El alcance es un backlog priorizado dinámicamente y guiado por la hipótesis del valor. El rol del Tech Lead es colaborar estrechamente con el Product Owner para dividir grandes iniciativas (Epics) en historias de usuario estimables y definir la versión mínima que valide el mercado (MVP).

---

## Alcance del Producto vs. Alcance del Proyecto

Es fundamental diferenciar qué se está construyendo del trabajo requerido para entregarlo:

* **Alcance del Producto:** Las características, requerimientos funcionales y no funcionales, y capacidades del entregable final. Se mide y valida frente a los **Requisitos del Producto** definidos en el Product Backlog.
* **Alcance del Proyecto:** Todo el trabajo y las actividades requeridas para entregar el producto con éxito (ej. pruebas de carga, configuración de infraestructura, reuniones de alineación). Se mide frente al **Plan de Dirección del Proyecto**.

---

## Gestión de Requisitos en Agile: El Backlog como Fuente de Verdad

En enfoques ágiles, la gestión del alcance ocurre de forma continua a través de la iteración. No se requiere un plan de gestión del alcance formal ni estático.

```text
  [Visión del Producto] + [Project Charter]
                   │
                   ▼
         [Definición del Alcance]
                   │
                   ▼
┌──────────────────────────────────────┐
│  Product Backlog (Artefacto Vivo)    │ <── Refinamiento continuo (PO + Devs)
└──────────────────────────────────────┘
                   │
                   ▼
┌──────────────────────────────────────┐
│  Sprint Backlog (Alcance de la Iter.)│ <── Fijo durante la ejecución del Sprint
└──────────────────────────────────────┘
```

El **Product Backlog** actúa como la única fuente de verdad y es gestionado activamente por el Product Owner, quien prioriza continuamente los requisitos según el valor comercial y la retroalimentación de los usuarios.

---

## El Enfoque del MVP (Henrik Kniberg)

El **Minimum Viable Product (MVP)** no es una versión incompleta o rota del producto. Según el modelo de Henrik Kniberg, es la menor cantidad de trabajo necesaria para validar una hipótesis de valor comercial con clientes reales de forma rápida.

```text
  NO RECOMENDADO (Orientado a Componentes):
  [Rueda] ──> [Chasis] ──> [Carrocería] ──> [Auto Completo] (Solo hay valor al final)

  RECOMENDADO (Orientado a Valor/MVP):
  [Skate] ──> [Monopatín] ──> [Bicicleta] ──> [Moto] ──> [Auto]
  (Cada iteración es Testable, Usable y Lovable; entrega transporte desde el día 1)
```

---

## La Estructura de Desglose de Trabajo (EDT/WBS)

La EDT/WBS es una descomposición jerárquica orientada al entregable del trabajo total que ejecutará el equipo del proyecto. 

### Reglas Clave:
1. **Regla del 100%**: La EDT debe contener el 100% del alcance del trabajo definido por el proyecto y capturar todos los entregables (tanto internos como externos y de gestión).
2. **Orientación a Entregables**: Los nodos de la EDT deben ser sustantivos (ej. *Base de datos configurada*) y no verbos de acción (ej. *Diseñar base de datos*).
3. **Paquete de Trabajo (Work Package)**: Es el nivel más bajo de la EDT. Debe poder ser estimado en costo y tiempo de manera confiable, y asignado a un único responsable.

### Ejemplo de Estructura EDT:

```text
1. Sistema de Comercio Electrónico (Proyecto)
   ├── 1.1 Infraestructura Cloud
   │   ├── 1.1.1 Servidor de Aplicaciones (Instancia EC2/AppEngine)
   │   └── 1.1.2 Base de Datos Relacional (PostgreSQL)
   ├── 1.2 Módulo de Clientes
   │   ├── 1.2.1 Autenticación (OAuth2 / JWT)
   │   └── 1.2.2 Portal de Gestión de Perfil
   ├── 1.3 Pasarela de Pagos
   │   ├── 1.3.1 API de Integración con Stripe
   │   └── 1.3.2 Sistema de Facturación y Notificaciones
   └── 1.4 Gestión del Proyecto
       ├── 1.4.1 Plan de Proyecto e Informes Mensuales
       └── 1.4.2 Documentación de Calidad y Pruebas
```

---

## Diccionario de la EDT/WBS

El diccionario de la EDT es el documento que detalla los requisitos, entregables y criterios de aceptación específicos para cada **Paquete de Trabajo** listado en la estructura jerárquica.

### Plantilla de Diccionario EDT:

| Campo | Descripción / Valor |
| :--- | :--- |
| **Código del Paquete de Trabajo** | *Ej. 1.2.1* |
| **Nombre del Paquete** | *Autenticación y Autorización de Clientes* |
| **Responsable** | *Líder Técnico de Backend / Equipo de Seguridad* |
| **Descripción del Trabajo** | Desarrollo de la infraestructura de backend para el registro de usuarios, login, renovación de tokens y protección de rutas privadas mediante tokens JWT firmados. |
| **Entregables Clave** | 1. API endpoints para registro, inicio de sesión y logout.<br>2. Base de datos con contraseñas encriptadas (bcrypt).<br>3. Documentación OpenAPI/Swagger de las rutas de seguridad. |
| **Criterios de Aceptación** | 1. Las contraseñas deben almacenarse usando hashing bcrypt con factor de costo >= 10.<br>2. Las solicitudes sin token JWT válido en rutas protegidas deben responder con HTTP 401 Unauthorized.<br>3. Cobertura de pruebas unitarias sobre el módulo de seguridad >= 85%. |
| **Hitos Relacionados** | Hito 1: Seguridad y Login Funcional (Fin del Mes 1). |
| **Recursos Requeridos** | 1 Ingeniero de Backend Senior, entorno de desarrollo y pruebas en Cloud. |

---

> [!TIP]
> **Pregunta de Entrevista de Big Tech (Product & Technical Leadership)**  
> *Estamos diseñando un nuevo servicio de mensajería en tiempo real. El Product Owner quiere lanzar el MVP con soporte para llamadas de video grupales, encriptación extremo a extremo, stickers personalizados e integración de bots. ¿Cómo actuarías como Tech Lead ante este requerimiento?*
> 
> **Respuesta Estratégica:**  
> 1. **Redefinir el MVP bajo el prisma de Kniberg (Earliest Testable/Usable/Lovable):** Le explicaría al PO que un MVP con demasiadas características complejas incrementa el riesgo técnico y el time-to-market. Dividimos la propuesta en hipótesis críticas a validar (ej. "¿Logramos una latencia menor a 100ms en mensajes de texto básicos con 1 millón de usuarios activos?").
> 2. **Identificar la funcionalidad núcleo:** El verdadero MVP "Lovable" y "Usable" de una app de mensajería es el envío de texto plano en tiempo real con confirmación de entrega (Double Check). Los stickers, bots y videollamadas son epics complementarias que aportan valor posterior, pero no validan el flujo primario.
> 3. **Proponer un Roadmap Iterativo:**
>    * *MVP 1 (Sprint 1-2):* Mensajes de texto 1 a 1 de latencia ultra baja (Core).
>    * *Versión 1.1 (Sprint 3-4):* Chats de grupo y encriptación básica.
>    * *Versión 1.2 (Sprint 5-6):* Llamadas de voz y stickers.
> Esto permite recibir feedback de producción temprano y optimizar la escalabilidad antes de añadir features pesados.
