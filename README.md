# Riesgo Relativo por Exposición a Contaminantes Atmosféricos en la ZMVM (2018–2022)

Este repositorio contiene el código fuente y los scripts utilizados en el análisis espacio-temporal del riesgo relativo de hospitalización por enfermedades respiratorias (asma, EPOC, neumonía, etc.) en la Zona Metropolitana del Valle de México, asociadas a contaminantes atmosféricos (NO₂, PM₁₀ y PM₂.₅) durante el periodo 2018–2022.

## 📌 Objetivo

Estimar el riesgo relativo (RR) de hospitalización por enfermedades respiratorias en función de los niveles de contaminación atmosférica, mediante modelos bayesianos espacio-temporales (BYM2), integrando variables ambientales y socioeconómicas.


## 🧪 Metodología

1. **Recopilación de datos:**
   - Contaminantes: RAMA y REDMET (SIMAT)
   - Hospitalizaciones: Secretaría de Salud (CIE-10)
   - Variables urbanas: CONAPO, DENUE-INEGI
   - Variables ambientales: Temperatura y humedad relativa

2. **Procesamiento en R:**
   - Limpieza, unión y transformación de paneles
   - Interpolación espacial (Kriging e IDW)
   - Análisis exploratorio (series de tiempo, correlaciones, desfases)

3. **Modelado Bayesiano (BYM2):**
   - Distribución: Binomial negativa
   - Covariables: NO₂, PM₁₀, PM₂.₅, TMP, HR, índice de marginación, densidad industrial
   - Inferencia vía INLA (`R-INLA` y `bmstdr`)

## ⚙️ Requisitos

- R ≥ 4.5.0
- Paquetes: `tidyverse`, `sf`, `ggplot2`, `INLA`, `bmstdr`, `spdep`, `raster`, `lubridate`
- PostgreSQL + PostGIS 

## 🔁 Reproducibilidad

Todos los scripts incluyen comentarios explicativos. Se sigue una lógica modular:
- `01_datos_salud.R`
- `02_variables_exposoma.R`
- `03_modelo_bayesiano.R`
- `04_resultados.R`

## 📄 Licencia

Distribuido bajo la **GNU General Public License v3.0**. Ver el archivo [LICENSE](LICENSE) para más detalles.

---

**Contacto:**  
Autoría académica colectiva  
Para más información, consulta la documentación incluida en el proyecto.
