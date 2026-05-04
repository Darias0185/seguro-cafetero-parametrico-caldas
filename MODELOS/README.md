# Modelos - Capa Predictiva

Esta carpeta contiene el desarrollo, entrenamiento y evaluación de los modelos utilizados para estimar la **producción mensual de café en Caldas**, como insumo para el diseño del seguro paramétrico.

---

##  Objetivo

Construir un modelo que estime la **producción esperada mensual**, integrando variables climáticas y patrones históricos, con el fin de:

- Mejorar la precisión frente a enfoques tradicionales  
- Capturar efectos diferidos del clima  
- Proveer un insumo para la activación del seguro  

---

##  Contenido

- `01_regresion.ipynb`  
  Modelo de regresión lineal con tendencia, estacionalidad y rezagos climáticos.

- `02_sarimax.ipynb`  
  Modelo de series de tiempo que incorpora dependencia temporal y estacionalidad anual.

- `03_random_forest.ipynb`  
  Modelo de ensamble que captura relaciones no lineales e interacciones complejas.

- `04_xgboost.ipynb`  
  Modelo de boosting secuencial que optimiza el aprendizaje sobre errores residuales.

---

##  Metodología

El enfoque sigue una progresión de complejidad:

1. **Regresión lineal**  
   Modelo base interpretable para establecer benchmark  

2. **SARIMAX**  
   Incorpora estructura temporal explícita  

3. **Random Forest**  
   Captura no linealidades y relaciones complejas  

4. **Gradient Boosting (XGBoost)**  
   Mejora la precisión mediante aprendizaje secuencial  

---

##  Métricas de evaluación

Los modelos se comparan usando:

- **RMSE:** penaliza errores grandes  
- **MAPE:** error porcentual interpretable  
- **MAE:** error promedio robusto  
- **R²:** capacidad explicativa  

La validación se realiza fuera de muestra mediante partición temporal (train/test).

---

##  Resultados principales

| Modelo | RMSE | MAPE | R² |
|--------|------|------|----|
| **Random Forest** | **10.56** | **11.71%** | **0.63** |
| XGBoost | 12.99 | 15.05% | 0.44 |
| Regresión | 14.06 | 14.57% | 0.34 |
| SARIMAX | 15.49 | 18.67% | 0.20 |

---

##  Hallazgos clave

- La relación clima–producción es **no lineal y con rezagos**  
- Los modelos de machine learning superan a los lineales  
- Random Forest logra el mejor desempeño  
- SARIMAX captura bien la estructura, pero con menor precisión  

---

##  Rol dentro del proyecto

Esta carpeta corresponde a la **capa predictiva**:

- Recibe el dataset del módulo ETL  
- Utiliza variables identificadas en EDA  
- Proporciona la producción esperada al módulo SPI  

---

##  Buenas prácticas

- Ejecutar notebooks completos  
- Mantener consistencia en partición temporal  
- No usar validación aleatoria en series de tiempo  
- Documentar interpretaciones dentro de cada notebook  

---
