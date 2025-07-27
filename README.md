# 🚕 Predicción de demanda en servicio de taxis: Sweet Lift Taxi

Proyecto de análisis y predicción de la demanda horaria de servicios de taxi en aeropuertos. El modelo busca anticipar la cantidad de pedidos de taxis en la próxima hora para mejorar la disponibilidad de conductores durante picos de demanda.

## 📌 Objetivo
Desarrollar un modelo de machine learning que prediga el número de pedidos de taxi por hora con una precisión aceptable (RMSE < 48), optimizando la planificación logística y operativa de la empresa Sweet Lift Taxi.

## 🧠 Metodología
1. **Análisis Exploratorio de Datos (EDA)**  
   - Revisión de estructura temporal y detección de tendencias y estacionalidad
   - Remuestreo de datos por hora para facilitar la modelación

2. **Creación de Features**  
   - Variables temporales: mes, día, día de la semana, hora
   - Series temporales: lags (1-4), medias móviles (7 horas), componentes de tendencia y estacionalidad

3. **Modelado Predictivo**  
   - Comparación de cinco modelos:
     - `LinearRegression`
     - `LightGBM`
     - `CatBoost`
     - `RandomForest`
     - `XGBoost`

4. **Evaluación**  
   - Métrica principal: RMSE
   - Análisis de rendimiento en conjunto de entrenamiento y prueba
   - Visualización de resultados para cada modelo

## 📈 Resultados
- Todos los modelos cumplieron con el criterio de RMSE < 48 en el conjunto de prueba.
- El modelo Random Forest obtuvo el mejor desempeño en datos no vistos.
- Se identificó una tendencia leve de sobreajuste, lo cual motivó recomendaciones de validación cruzada y segmentación más robusta.

## 🛠️ Tecnologías utilizadas
| Herramientas              | Propósito                          |
|---------------------------|------------------------------------|
| `Pandas`, `Numpy`         | Manipulación de datos              |
| `Matplotlib`, `Seaborn`   | Visualización exploratoria         |
| `LightGBM`, `CatBoost`, `XGBoost`, `RandomForest` | Modelos predictivos     |
| `seasonal_decompose`      | Análisis de series temporales      |
| `train_test_split`        | División de datos                  |
| `mean_squared_error`, `RMSE` | Evaluación de desempeño del modelo |

## 📁 Estructura del repositorio
```text
├── notebooks/
│   └── taxi_demand_analysis.ipynb
├────── datasets/
│       └── taxi.csv
├── images/
│   └── rmse_comparison.png
│   └── estacionalidad.png
│   └── Ordenes_por_hora.png
├── README.md
