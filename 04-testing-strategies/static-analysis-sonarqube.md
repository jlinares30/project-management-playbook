# Análisis Estático con SonarQube: Controlando la Deuda Técnica

El análisis estático de código examina el código fuente sin ejecutar el programa, buscando fallos de diseño, vulnerabilidades de seguridad, violaciones de estándares de estilo y código duplicado.

---

## La Deuda Técnica

La **Deuda Técnica** es una metáfora que describe el costo futuro de optar por soluciones de software rápidas y fáciles a corto plazo, en lugar de utilizar un enfoque técnico óptimo a largo plazo.

### Tipos de Deuda Técnica (Cuadrante de Martin Fowler)
* **Reventada e Imprudente**: "No tenemos tiempo para diseñar o escribir pruebas".
* **Imprudente e Inadvertida**: "¿Qué es un patrón de diseño?".
* **Prudente y Deliberada**: "Debemos entregar ya, luego refactorizaremos esto".
* **Prudente e Inadvertida**: "Ahora sabemos cómo deberíamos haber diseñado esto al inicio".

*Métrica asociada (SQALE)*: **Índice de Deuda Técnica** (estimación en días u horas requeridas para solucionar los problemas detectados en el código).

---

## Cobertura de Código (Code Coverage)

La cobertura de código indica qué porcentaje de nuestro código fuente ha sido ejecutado por la suite de pruebas unitarias o de integración.

### Tipos de Métricas de Cobertura:
1. **Cobertura de Líneas (Line Coverage)**: Porcentaje de líneas de código individuales ejecutadas por al menos una prueba.
2. **Cobertura de Ramas (Branch/Decision Coverage)**: Valida si cada punto de decisión (como sentencias `if-else` o declaraciones `switch`) ha sido evaluado en sus caminos verdadero y falso.
3. **Cobertura de Funciones (Function Coverage)**: Cantidad de funciones declaradas que se invocaron en las pruebas.

*Recomendación de la industria*: Apuntar a una cobertura mínima del **80%** en componentes críticos. Exigir 100% de manera absoluta suele llevar a pruebas triviales o de poco valor real.

---

## Puertas de Calidad (Quality Gates) con SonarQube

SonarQube es la herramienta líder para analizar la salud técnica de los proyectos. Configurar una **Quality Gate** en el pipeline garantiza que ningún código nuevo degrade la calidad actual del proyecto.

### Métricas Típicas de una Quality Gate para Código Nuevo (New Code):

| Métrica | Umbral Recomendado | Descripción |
| :--- | :--- | :--- |
| **Bugs** | `0` (Rating A) | Ningún error de lógica abierto. |
| **Vulnerabilities** | `0` (Rating A) | Cero agujeros de seguridad potenciales en el código nuevo. |
| **Security Hotspots Approved**| `100%` | Todos los puntos calientes de seguridad marcados deben ser revisados. |
| **Technical Debt Ratio** | `< 5.0%` | La deuda técnica acumulada en el código nuevo debe ser mínima. |
| **Coverage on New Code** | `>= 80.0%` | El código nuevo debe venir debidamente probado. |
| **Duplicated Lines** | `< 3.0%` | Evitar la duplicación de bloques de código (DRY - Don't Repeat Yourself). |
