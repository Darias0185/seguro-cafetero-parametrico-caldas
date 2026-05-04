# ETL - Construcción del dataset

Esta carpeta contiene los procesos de extracción, transformación y carga de datos utilizados para construir el dataset maestro del proyecto.

## Fuentes de datos
- Precipitación (CHIRPS)
- NDVI (MODIS)
- Producción cafetera
- Precios del café

## Proceso
El notebook `01_construccion_dataset.ipynb` integra las fuentes, genera variables derivadas y construye el dataset final utilizado en los modelos.

## Output
El resultado de este proceso es el dataset:
`cafe_seguro_master.csv`
