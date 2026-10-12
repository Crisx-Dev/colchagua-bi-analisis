# Análisis BI — Vulnerabilidad Territorial en Colchagua

Proyecto de Business Intelligence sobre la vulnerabilidad territorial de la provincia de Colchagua (Región de O'Higgins, Chile), en el período 2018-2021.

##  Descripción

Análisis cruzado de datos climáticos, económicos y territoriales para identificar qué comunas y PYMEs de la provincia están más expuestas a shocks externos. El proyecto integra cuatro fuentes oficiales y aplica técnicas de ETL, modelado dimensional y machine learning.

##  Objetivo

Responder la pregunta: *¿Qué comunas, sectores y PYMEs de la provincia de Colchagua son más vulnerables a que un shock sobre la agricultura se propague sobre su economía?*

##  Contenido del repositorio

### Reporte Power BI
- `powerbi/colchagua.pbix` — Reporte completo con 5 páginas:
  - **Contexto**: panorama general y ventas por comuna
  - **Vulnerabilidad**: ranking y perfil de amenazas
  - **Amenazas**: análisis de calor, heladas e incendios
  - **Forecast**: proyecciones 2022-2023
  - **Análisis Varios**: efecto dominó y análisis sectorial

### Notebooks de análisis
- `notebooks/01_etl_limpieza.ipynb` — Pipeline ETL y limpieza de datos
- `notebooks/02_eda_analisis_exploratorio.ipynb` — Análisis exploratorio
- `notebooks/03_clustering_kmeans.ipynb` — Clustering territorial (k=2)
- `notebooks/04_forecast_holt_winters.ipynb` — Proyección de escasez hídrica

##  Stack técnico

- **Análisis:** Python (pandas, numpy, scikit-learn, statsmodels)
- **Visualización:** Power BI, DAX
- **Modelado:** Datamart en esquema estrella (6 dimensiones, 5 tablas de hechos)

##  Fuentes de datos

- **SII** — Empresas por comuna y actividad (CIIU 4 dígitos)
- **CIREN/ODEPA** — Catastro Frutícola Nacional
- **CONAF** — Incendios forestales por comuna
- **Open-Meteo** — Reanálisis ERA5 (series diarias)

Todas las fuentes son oficiales y públicas, garantizando la trazabilidad del análisis.

##  Cómo usar el reporte

1. Descarga el archivo `colchagua.pbix` desde la carpeta `powerbi/`.
2. Ábrelo con **Power BI Desktop** (descarga gratuita en [powerbi.microsoft.com](https://powerbi.microsoft.com/desktop/)).
3. Explora las 5 páginas usando los filtros por comuna, año y actividad.

## 📄 Licencia

Proyecto académico. Los datos utilizados son de fuentes públicas oficiales.