# EDA - Análisis Descriptivo

Esta carpeta contiene el análisis exploratorio de datos (**Exploratory Data Analysis - EDA**) del proyecto de seguro cafetero paramétrico en Caldas.

---

##  Objetivo

Caracterizar el comportamiento histórico de la producción cafetera y su relación con variables climáticas, con el fin de:

- Identificar patrones de estacionalidad  
- Detectar eventos extremos  
- Analizar la relación clima–producción  
- Fundamentar el diseño del modelo predictivo  
- Evaluar las limitaciones del índice SPI  

---

##  Contenido

- `02_analisis_descriptivo.ipynb`  
  Notebook que desarrolla el análisis completo del dataset maestro, incluyendo:
  - Estadísticas descriptivas  
  - Análisis temporal  
  - Estacionalidad mensual  
  - Correlaciones  
  - Análisis con rezagos  

---

##  Principales análisis realizados

### 1. Estadísticas descriptivas
- Media, dispersión y rango de la producción  
- Comparación con precipitación y NDVI  
- Identificación de variabilidad y eventos extremos  

---

### 2. Comportamiento temporal
- Estacionalidad bimodal del café en Caldas  
- Identificación de la crisis 2009–2013  
- Cambios estructurales en la producción  

---

### 3. Estacionalidad mensual
- Picos de producción (cosecha principal y mitaca)  
- Relación con el patrón de lluvias  
- Variabilidad interanual  

---

### 4. Relación clima–producción
- Análisis de correlación  
- Evaluación de precipitación y NDVI  

---

### 5. Análisis con rezagos
- Efecto diferido del clima sobre la producción  
- Identificación de rezagos relevantes (1–6 meses)  
- Cambios en la dirección del efecto según el ciclo agrícola  

---

##  Hallazgos clave

- La relación entre clima y producción es:
  - **No lineal**
  - **Diferida (con rezagos)**
  - **Dependiente del ciclo productivo**

- Ni la precipitación ni el NDVI explican la producción en el mismo mes  

- El índice SPI captura solo parcialmente el comportamiento climático relevante  

---

##  Rol dentro del proyecto

El EDA constituye la **capa descriptiva** del sistema analítico y cumple un rol fundamental:

- Define las variables del modelo  
- Justifica el uso de rezagos  
- Evidencia limitaciones del SPI  
- Orienta la selección de técnicas de machine learning  

---

##  Relación con otras capas

- **ETL:** provee el dataset maestro  
- **Modelos:** utiliza las variables identificadas en el análisis  
- **SPI:** se evalúa a la luz de los hallazgos del EDA  

---

##  Buenas prácticas

- Ejecutar el notebook completo para reproducibilidad  
- Mantener coherencia entre gráficos y análisis  
- Documentar interpretaciones clave dentro del notebook  

---
