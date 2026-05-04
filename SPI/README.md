# SPI - Índice Paramétrico de Activación

Esta carpeta contiene la construcción, evaluación e integración del **Índice de Precipitación Estandarizado (SPI)** dentro del diseño del seguro cafetero paramétrico.

---

##  Objetivo

Analizar el desempeño del SPI como trigger del seguro y desarrollar un esquema mejorado que reduzca el *basis risk* mediante su integración con modelos predictivos de producción.

---

##  Contenido

- `06_indice_spi.ipynb`  
  - Cálculo del SPI en diferentes escalas  
  - Análisis del comportamiento del índice  
  - Identificación de eventos extremos  
  - Evaluación de su relación con la producción  

- `07_integracion_spi_modelo.ipynb`  
  - Integración del SPI con la producción esperada (modelo predictivo)  
  - Análisis de discrepancias entre activación y pérdidas reales  
  - Evaluación del desempeño del esquema híbrido  
  - Propuesta de mejora del trigger del seguro  

---

##  Metodología

El enfoque se desarrolla en dos etapas:

### 1. Evaluación del SPI
- Cálculo en múltiples ventanas (SPI-6, SPI-9)  
- Identificación de eventos climáticos  
- Comparación con producción real  

### 2. Integración con modelo
- Uso de producción esperada (Random Forest)  
- Análisis de desviaciones respecto a niveles normales  
- Evaluación de activación vs pérdidas  

---

##  Hallazgos clave

- El SPI por sí solo presenta limitaciones para reflejar el impacto productivo  
- Se identifican casos de:
  - Activación sin pérdida  
  - Pérdida sin activación  

- La integración con el modelo mejora la capacidad de detección de eventos relevantes  

---

##  Propuesta de mejora

Se plantea un esquema híbrido:

- **SPI-9:** define la activación del evento  
- **SPI-6:** determina la intensidad del pago  
- **Modelo predictivo:** valida impacto productivo  

---

##  Rol dentro del proyecto

Esta carpeta corresponde a la **capa de activación**:

- Recibe insumos del ETL  
- Utiliza resultados de modelos  
- Define el trigger del seguro  

---

##  Buenas prácticas

- Ejecutar notebooks completos  
- Validar consistencia temporal  
- Interpretar resultados junto con producción y NDVI  

---
