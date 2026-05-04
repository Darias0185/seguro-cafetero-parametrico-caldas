#  Seguro Cafetero Paramétrico Indexado – Caldas

Proyecto de analítica para la MIAD, orientado a mejorar la activación de seguros paramétricos cafeteros en Caldas, reduciendo la desalineación entre el índice climático (SPI) y el impacto real en la producción.

---

## Problema

El seguro paramétrico actual basado en el **SPI (Standardized Precipitation Index)** presenta una falla estructural:

- Se activa sin que exista caída en la producción  
- No se activa cuando sí hay pérdidas reales  

Esto genera **desconfianza en el caficultor** y limita la adopción del seguro.

---

##  Solución propuesta

Se desarrolla un artefacto analítico en tres capas:

### 1. Capa descriptiva
- Análisis histórico (2002–2025)
- Estacionalidad bimodal del café
- Relación clima–producción con rezagos

### 2. Capa predictiva
Estimación de la producción esperada mensual usando:
- Precipitación (CHIRPS)
- NDVI (MODIS)
- Variables rezagadas

**Modelos evaluados:**
- Regresión lineal con rezagos  
- SARIMAX  
- Random Forest  
- Gradient Boosting  

### 3. Capa de activación
Recalibración del índice SPI mediante un esquema híbrido:

- **SPI-9 → Activación del evento (persistencia)**
- **SPI-6 → Intensidad del pago (severidad)**

---

##  Resultados principales

| Modelo | RMSE | MAPE | R² |
|--------|------|------|----|
| **Random Forest (ganador)** | **10.56** | **11.71%** | **0.63** |
| Gradient Boosting | 12.99 | 15.05% | 0.44 |
| Regresión | 14.06 | 14.57% | 0.34 |
| SARIMAX | 15.49 | 18.67% | 0.20 |

✔ Cumple requerimiento de error (<15%)  
✔ Supera benchmark de literatura (~16%)

---

##  Hallazgo clave

El índice SPI actual no refleja adecuadamente el impacto productivo:

- **Condiciones secas → pagos altos sin caída productiva**
- **Condiciones húmedas → caídas productivas sin activación**

 El problema es **estructural**, no solo de calibración.

---

##  Estructura del repositorio

```bash
Dataset_maestro/   # Datos integrados y dataset final
ETL/               # Procesos de limpieza e integración
Modelos/           # Modelos entrenados (.pkl)
SPI/               # Construcción y calibración del índice
