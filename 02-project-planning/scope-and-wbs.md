# Alcance y WBS/EDT (Estructura de Desglose de Trabajo)

La definición y descomposición precisa del alcance evita la corrupción del alcance (*scope creep*) y asegura que todas las partes interesadas compartan la misma visión de los entregables del proyecto.

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
