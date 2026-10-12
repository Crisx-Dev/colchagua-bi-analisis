# Análisis BI — Vulnerabilidad Territorial en Colchagua

Proyecto de Business Intelligence sobre la vulnerabilidad territorial de la provincia de Colchagua (Región de O'Higgins, Chile), en el período 2018-2021.

## Descripción

Análisis cruzado de datos climáticos, económicos y territoriales para identificar qué comunas y PYMEs de la provincia están más expuestas a shocks externos. El proyecto integra cuatro fuentes oficiales y aplica técnicas de ETL, modelado dimensional y machine learning.

## Objetivo

Responder la pregunta: ¿Qué comunas, sectores y PYMEs de la provincia de Colchagua son más vulnerables a que un shock sobre la agricultura se propague sobre su economía?

## Contenido del repositorio

### Reporte Power BI

`powerbi/colchagua.pbix` — Reporte completo con 5 páginas:

- **Contexto**: panorama general y ventas por comuna.
- **Vulnerabilidad**: ranking y perfil de amenazas.
- **Amenazas**: análisis de calor, heladas e incendios.
- **Forecast**: proyecciones 2022-2023.
- **Análisis Varios**: efecto dominó y análisis sectorial.

### Notebooks de análisis

- `notebooks/ETL_Forecast.ipynb` — Pipeline ETL, limpieza de datos y proyecciones.

## Stack técnico

- **Análisis**: Python (pandas, numpy, scikit-learn, statsmodels)
- **Visualización**: Power BI, DAX
- **Modelado**: Datamart en esquema estrella (6 dimensiones, 5 tablas de hechos)

## Fuentes de datos

- **SII** — Empresas por comuna y actividad (CIIU 4 dígitos)
- **CIREN/ODEPA** — Catastro Frutícola Nacional
- **CONAF** — Incendios forestales por comuna
- **Open-Meteo** — Reanálisis ERA5 (series diarias)

Todas las fuentes son oficiales y públicas, garantizando la trazabilidad del análisis.

## Cómo usar el reporte

1. Descarga el archivo `colchagua.pbix` desde la carpeta `powerbi/`.
2. Ábrelo con Power BI Desktop (descarga gratuita en powerbi.microsoft.com).
3. Explora las 5 páginas usando los filtros por comuna, año y actividad.

## Declaración de uso de Inteligencia Artificial

En conformidad con las directrices de la industria del dato, se declara el uso transparente de Inteligencia Artificial como herramienta de aceleración tecnológica:

- **Herramientas**: Google Gemini y DeepSeek
- **Tareas asistidas**: Apoyo en la auditoría estructural del modelo de datos, generación de scripts visuales en Python y asistencia en la implementación del sitio web del portafolio.
- **Responsabilidad humana**: La formulación abierta del problema, la estrategia de selección cruzada de fuentes gubernamentales, la validación del HHI de monocultivo, la corrección de falsos positivos económicos y la interpretación de los hallazgos de negocio son autoría intelectual exclusiva de los alumnos, quienes comprenden y defienden cada decisión técnica documentada.

## Autores

- Cristóbal Vargas
- Juan Riveros

Ingeniería de Ejecución en Informática — Instituto Profesional AIEP
Curso: ISI802 — Business Intelligence (2026)

## Licencia

Proyecto académico. Los datos utilizados son de fuentes públicas oficiales.
