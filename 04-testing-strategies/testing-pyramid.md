# La Pirámide de Pruebas: Estrategias de Validación de Software

La pirámide de pruebas es un modelo conceptual que agrupa las pruebas de software por su nivel de granularidad, velocidad y costo de mantenimiento. Su objetivo es balancear el esfuerzo de automatización para optimizar el feedback de desarrollo.

---

## Estructura de la Pirámide de Pruebas

```text
              ▲
             / \
            /   \      E2E / UI (Lentas, Costosas, Frágiles)
           / E2E \     --> Cypress, Playwright, Selenium
          /-------\
         / Integr. \   Integración / Contract (Velocidad Media)
        /-----------\  --> Supertest, Pact, Spring MockMvc
       / Unitarias   \ Unitarias (Muy Rápidas, Baratas, Estables)
      /_______________\ --> Jest, Mocha, JUnit, PyTest
```

### 1. Pruebas Unitarias (Unit Tests)
* **Objetivo**: Validar el comportamiento de la unidad de código más pequeña y aislada posible (ej. funciones, métodos, clases individuales).
* **Aislamiento**: Obligatorio. Se deben utilizar dobles de prueba (*mocks*, *stubs*, *spies*) para aislar bases de datos, APIs de red y otras clases.
* **Proporción**: Deben constituir el **70-80%** del total de la suite de pruebas debido a su rapidez de ejecución (milisegundos) y bajo costo.

### 2. Pruebas de Integración (Integration Tests)
* **Objetivo**: Verificar que múltiples componentes funcionen bien juntos (ej. controlador interactuando con la base de datos o el gestor de caché).
* **Alcance**: Pueden requerir contenedores locales (ej. *Testcontainers* con Docker) para levantar instancias reales pero temporales de bases de datos.

### 3. Pruebas de Contrato (Contract Testing)
* **Objetivo**: Asegurar que los microservicios proveedores y consumidores coincidan en la estructura de datos que intercambian (el "contrato") sin necesidad de desplegarlos juntos.
* **Herramientas**: *Pact*. Previene que cambios en el formato de API del backend rompan silenciosamente al cliente frontend en producción.

### 4. Pruebas de Extremo a Extremo (E2E Tests)
* **Objetivo**: Simular el flujo real del usuario final a través de la interfaz visual e interactuando con todo el ecosistema (Frontend, Backend, base de datos de pruebas).
* **Consideración**: Deben ser limitadas (ej. **5-10%**) porque son lentas, propensas al parpadeo (*flaky tests*) y complejas de mantener.

---

## Pruebas No Funcionales (NFR Testing)

* **Pruebas de Rendimiento y Carga (Load/Stress Testing)**: Validar cómo responde la infraestructura bajo cargas normales e inusuales. Herramientas: *k6*, *JMeter*.
* **Pruebas de Seguridad (DAST/SAST)**: Análisis dinámico y estático buscando fallos de seguridad e inyección de dependencias vulnerables. Herramientas: *OWASP ZAP*, *Snyk*.
* **Pruebas de Accesibilidad (A11y)**: Garantizar que el sistema sea accesible para personas con discapacidades bajo la norma WCAG. Herramientas: *Axe-core*.
