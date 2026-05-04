# ETL - Construcción del Dataset Maestro

Esta carpeta contiene el proceso de **Extracción, Transformación y Carga (ETL)** utilizado para construir el dataset maestro del proyecto de seguro cafetero paramétrico en Caldas.

---

##  Objetivo

Integrar y transformar múltiples fuentes de información climática, satelital y productiva en una serie temporal mensual consistente, que sirva como base para:

- Modelación de la producción cafetera  
- Análisis de la relación clima–producción  
- Evaluación del índice paramétrico (SPI)  

---

##  Contenido

- `01_construccion_dataset.ipynb`  
  Notebook principal que implementa el pipeline completo de ETL:
  - Ingesta de datos
  - Limpieza y validación
  - Transformaciones temporales
  - Construcción de variables
  - Integración de fuentes
  - Generación del dataset final  

---

##  Fuentes de datos

El proceso integra las siguientes fuentes:

- **Precipitación:** CHIRPS (datos satelitales)  
- **Vegetación:** NDVI (MODIS)  
- **Producción cafetera:** series históricas departamentales  
- **Precios del café:** información económica complementaria  

---

##  Pipeline de transformación

El flujo ETL sigue una lógica secuencial:

1. **Extracción:** carga de datos desde múltiples formatos y fuentes  
2. **Limpieza:** tratamiento de valores faltantes y validación de consistencia  
3. **Estandarización:** conversión a frecuencia mensual  
4. **Transformación:** generación de variables derivadas  
5. **Integración:** unión de todas las fuentes en una sola base  
6. **Validación:** verificación de integridad y cobertura temporal  
7. **Exportación:** generación del dataset final  

---

##  Output

El resultado del proceso es:

```text
cafe_seguro_master.csv
