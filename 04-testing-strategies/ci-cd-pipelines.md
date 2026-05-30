# Pipelines de CI/CD: Automatización y Control de Calidad en Producción

La integración continua (CI) y el despliegue continuo (CD) permiten que el software se valide y se lance a producción de forma consistente y libre de errores manuales.

---

## Flujo de un Pipeline de CI/CD Estándar

El pipeline actúa como un embudo de calidad (Quality Gate). Si una etapa falla, el pipeline se detiene inmediatamente y la compilación se marca como fallida.

```text
[Commit en Git]
      │
      ▼
┌──────────────┐
│  1. Build    │ ──> Compilar el código y validar dependencias
└──────────────┘
      │
      ▼
┌──────────────┐
│  2. Lint/Sec │ ──> Linters (ESLint, Prettier) y escaneo de vulnerabilidades
└──────────────┘
      │
      ▼
┌──────────────┐
│  3. Test     │ ──> Ejecución de pruebas unitarias y de integración
└──────────────┘
      │
      ▼
┌──────────────┐
│  4. QA Gate  │ ──> Cobertura de código y análisis estático (SonarQube)
└──────────────┘
      │
      ▼
┌──────────────┐
│  5. Deploy   │ ──> Despliegue automatizado en entornos (Staging / Prod)
└──────────────┘
```

---

## Políticas de Branch Protection (Protección de Ramas)

Para evitar la corrupción del código base principal (`main` o `master`), se deben configurar las siguientes reglas en plataformas como GitHub o GitLab:

1. **Requerir Pull Request para fusionar**: No se permite hacer `git push` directo a ramas principales.
2. **Aprobación de pares (Peer Review)**: Al menos 1 o 2 desarrolladores aprobados deben revisar el código antes de la fusión.
3. **Verificaciones de estado exitosas (Status Checks)**: El pipeline de CI debe compilar y pasar el 100% de las pruebas antes de habilitar el botón "Merge".
4. **Cerrar historial lineal (Optional)**: Requerir *Squash and Merge* para mantener la historia de commits limpia.

---

## Ejemplo Práctico: GitHub Actions Pipeline Config (`.github/workflows/ci.yml`)

```yaml
name: CI/CD Pipeline

on:
  push:
    branches: [ main, develop ]
  pull_request:
    branches: [ main ]

jobs:
  build-and-test:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout Code
      uses: actions/checkout@v3

    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 18
        cache: 'npm'

    - name: Install Dependencies
      run: npm ci

    - name: Run Linters and Format Check
      run: npm run lint

    - name: Run Unit and Integration Tests
      run: npm run test:cov

    - name: Upload Test Coverage
      uses: actions/upload-artifact@v3
      with:
        name: coverage-report
        path: coverage/
```
