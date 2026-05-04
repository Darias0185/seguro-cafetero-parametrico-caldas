# SPI - Índice Paramétrico de Activación

Esta carpeta contiene la construcción, análisis y calibración del **Índice de Precipitación Estandarizado (SPI)** utilizado como mecanismo de activación del seguro cafetero paramétrico.

---

##  Objetivo

Evaluar la capacidad del índice SPI para reflejar condiciones agroclimáticas que afectan la producción cafetera en Caldas, y proponer mejoras en su diseño para reducir el *basis risk*.

---

##  Contenido

- `06_indice_spi.ipynb`  
  Notebook principal donde se desarrolla:
  - Cálculo del SPI en diferentes ventanas temporales  
  - Análisis del comportamiento del índice  
  - Comparación con la producción cafetera  
  - Evaluación de discrepancias  
  - Propuesta de calibración del índice  

---

##  Metodología

El análisis del SPI incluye:

1. Cálculo del índice en distintas escalas temporales (ej: SPI-6, SPI-9)  
2. Identificación de eventos extremos (sequía/exceso de lluvia)  
3. Comparación con la producción observada  
4. Evaluación del desalineamiento entre índice y pérdidas reales  
5. Ajuste de ventanas para mejorar la activación del seguro  

---
##  Hallazgos clave

- El SPI presenta limitaciones para capturar el impacto real sobre la producción  
- Existen casos de:
  - Activación sin pérdida productiva  
  - Pérdidas sin activación del índice  

- El problema es estructural y se relaciona con:
  - Falta de incorporación de rezagos  
  - Ausencia de variables de vegetación  

---

##  Propuesta de mejora

Se plantea un esquema híbrido:

- **SPI-9:** define la activación del evento (persistencia climática)  
- **SPI-6:** determina la intensidad del pago  

Este enfoque mejora la correspondencia entre clima y producción.

---

##  Relación con el proyecto

Esta carpeta corresponde a la **capa de activación** del sistema:

- Recibe insumos del ETL y modelos  
- Se integra con la producción esperada  
- Define cuándo el seguro debe activarse  

---

##  Buenas prácticas

- Ejecutar el notebook completo para reproducibilidad  
- Validar consistencia temporal del índice  
- Interpretar resultados junto con producción y NDVI  

---
