# Seguridad de la Información en el Ciclo de Vida del Software

> [!NOTE]
> **Seguridad como Atributo de Calidad No Funcional**
> En la ingeniería de software moderna, la seguridad no es una preocupación aislada que se gestiona una vez que la aplicación está en producción. Debe integrarse activamente en todas las fases del ciclo de vida del software (enfoque de **DevSecOps**), asegurando que el código sea seguro por diseño.

---

## 1. La Tríada CIA

El pilar fundamental de la seguridad de la información consiste en la preservación de tres principios básicos sobre los activos de información:

```text
                        ┌────────────────────────┐
                        │   Seguridad de la      │
                        │     Información        │
                        └───────────┬────────────┘
            ┌───────────────────────┼───────────────────────┐
            ▼                       ▼                       ▼
   Confidencialidad            Integridad             Disponibilidad
 (Acceso solo autorizado)  (Información exacta)    (Sistemas accesibles)
```

1. **Confidencialidad (Confidentiality):** Garantizar que la información sea accesible únicamente para aquellas personas o sistemas que cuenten con la autorización correspondiente (ej. encriptación de datos, control de accesos basado en roles).
2. **Integridad (Integrity):** Salvaguardar la exactitud y completitud de la información y sus métodos de procesamiento, evitando modificaciones no autorizadas o accidentales (ej. firmas digitales, hashes de verificación).
3. **Disponibilidad (Availability):** Asegurar que los usuarios autorizados tengan acceso a la información y a los activos asociados cuando lo requieran (ej. sistemas de alta disponibilidad, redundancia, planes de recuperación ante desastres).

---

## 2. Sistema de Gestión de la Seguridad de la Información (SGSI)

Un **SGSI** (basado en el estándar internacional **ISO/IEC 27001**) es el conjunto de políticas, procedimientos, directrices y recursos asociados que una organización define y formaliza para gestionar y controlar sistemáticamente los riesgos de seguridad sobre sus activos de información.

### Objetivos Principales de un SGSI
* Proteger de forma proactiva los activos de información críticos de la empresa (incluyendo el código fuente y las bases de datos).
* Evaluar y mitigar de manera continua los riesgos asociados a la seguridad.
* Establecer un comité y gobierno formal de seguridad con roles de propietarios de activos e información.
* Responder e instrumentar protocolos de contingencia inmediatos ante incidentes.

### Clasificación de la Información
Para aplicar controles proporcionales a los riesgos, las organizaciones estructuran la información en categorías de confidencialidad:

* **Confidencial (Strictly Confidential):** Información crítica cuya divulgación no autorizada causaría graves perjuicios financieros, legales o de reputación (ej. datos de tarjetas de crédito, contraseñas, código fuente de algoritmos propietarios). Exige acuerdos de confidencialidad (NDA) y cifrado estricto.
* **Restringido (Restricted):** Información operativa clave destinada únicamente a un área o proceso de negocio específico (ej. arquitectura de red, reportes de vulnerabilidades de TI). Su filtración puede afectar operaciones internas.
* **Uso Interno (Internal Use):** Información destinada para consumo general de todos los empleados de la empresa, que no representa mayor impacto si se divulga, pero no es de acceso público (ej. políticas internas, organigramas).

---

## 3. Controles Técnicos en el Desarrollo de Software (ISO/IEC 27002:2022)

Para garantizar un ciclo de vida de desarrollo de software seguro, se aplican controles del estándar **ISO/IEC 27002**:

### A. Gestión de Accesos y Autenticación
* **Acceso basado en necesidad (Least Privilege):** El nivel de acceso a los entornos de desarrollo, bases de datos y servidores de producción debe restringirse estrictamente según las necesidades del rol del empleado.
* **Políticas de Contraseñas Robustas:** Contraseñas personales con una longitud mínima de 8 a 12 caracteres, mezclando mayúsculas, minúsculas, números y caracteres especiales, complementadas con Autenticación de Doble Factor (2FA).

### B. Protección contra Malware y Vulnerabilidades
* **Herramientas Anti-Malware Automatizadas:** Instalación de software de protección en endpoints y servidores, configurando escaneos continuos sobre archivos entrantes/salientes y peticiones de red.
* **Análisis de Vulnerabilidades (Vulnerability Scanning):** Pruebas y escaneos automáticos de vulnerabilidades técnicas sobre el código y dependencias de terceros programados anualmente o integrados de forma continua en el pipeline de CI/CD (ej. análisis de dependencias OWASP Dependency-Check).

### C. Continuidad: Backups y Restore
* **Backups del Sistema:** Copias de respaldo automáticas y cifradas de la información crítica del negocio y bases de datos. Los accesos para realizar backups deben estar restringidos al personal autorizado.
* **Pruebas de Restauración (Restore Tests):** Los backups no sirven de nada si no se pueden restaurar. Se deben establecer cronogramas regulares para comprobar la validez de los backups mediante simulacros de restauración documentados formalmente.

### D. Controles Criptográficos
* **Cifrado de Datos:** Uso de algoritmos robustos para encriptar claves de acceso y proteger datos tanto en tránsito (ej. HTTPS, TLS) como en reposo (ej. cifrado de bases de datos).
* **Administración de Claves (Key Management):** Procedimientos rigurosos para la generación, almacenamiento, rotación y recuperación de llaves criptográficas.

---

## 4. Cumplimiento Legal y Privacidad de Datos

El desarrollo de software debe cumplir con el marco regulatorio del país donde opera el negocio y donde residen sus usuarios.

* **Protección de Datos Personales:** Implementar por diseño los principios de consentimiento, finalidad y seguridad para proteger los datos identificativos de los usuarios (ej. en el contexto de Perú, cumplir estrictamente con la **Ley de Protección de Datos Personales - Ley Nº 29733** y su Reglamento).
* **Anonimización y Seudonimización:** Técnicas indispensables para enmascarar datos de producción reales antes de utilizarlos en bases de datos para pruebas y control de calidad (QA).
