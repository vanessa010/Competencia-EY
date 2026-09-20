# Competencia-EY

# EY AI & Data Challenge: Water Quality Prediction in South Africa

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Competition](https://img.shields.io/badge/EY%20Challenge-Optimizing%20Clean%20Water-orange.svg)](https://challenge.ey.com/)

Repositorio con la solución desarrollada para el **EY AI & Data Challenge**, enfocado en la estimación y monitoreo de la calidad del agua en cuerpos fluviales de Sudáfrica mediante Machine Learning, teledetección (remote sensing) y variables climáticas.

---

##  1. Descripción del Desafío

El acceso a agua limpia y segura es uno de los mayores retos globales (ODS 6 de la ONU). En muchas regiones de África, el monitoreo físico continuo de ríos y embalses resulta costoso y logísticamente inviable.

El objetivo de esta competencia es entrenar modelos de aprendizaje automático capaces de **predecir parámetros clave de calidad del agua** en ríos a partir de:
- Mediciones históricas in-situ (2011–2015) en ~200 estaciones de muestreo en Sudáfrica.
- Imágenes satelitales ópticas e índices espectrales (Landsat).
- Variables meteorológicas y de balance hídrico (TerraClimate).

###  Variables Objetivo (Targets)
1. **Total Alkalinity (Alcalinidad Total):** Capacidad del agua para neutralizar ácidos.
2. **Electrical Conductance (Conductividad Eléctrica):** Indicador de sales disueltas y concentración iónica total.
3. **Dissolved Reactive Phosphorus (Fósforo Reactivo Disuelto):** Nutriente crítico causante de eutrofización y proliferación de algas.

> **Reto Clave (Generalización Espacial):** El conjunto de prueba/validación evalúa estaciones en **cuencas y regiones geográficas no vistas** durante el entrenamiento. Los modelos no pueden memorizar coordenadas; deben aprender relaciones físicas y ambientales generalizables.

---

##  2. Fuentes de Datos

| Fuente | Tipo de Datos | Variables Principales |
| :--- | :--- | :--- |
| **Ground Truth (EY)** | Mediciones de campo | Fecha, Latitud, Longitud, Valores objetivo de calidad del agua. |
| **Landsat (Microsoft Planetary Computer / GEE)** | Satelital / Reflectancia | Bandas ópticas (RGB, NIR, SWIR), índices espectrales (NDWI, MNDWI, NDVI, turbidity proxy). |
| **TerraClimate** | Reanálisis climático mensual | Precipitación, temperatura máxima/mínima, evapotranspiración, escorrentía, déficit hídrico del suelo. |
| **DEM / Topografía (Opcional)** | Elevación | Pendiente, elevación de la cuenca, acumulación de flujo. |

---

