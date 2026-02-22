# 🏠 Modelado Predictivo de Precios de Vivienda

## 📌 Contexto del Negocio
En el mercado inmobiliario, la tasación manual de propiedades es un proceso costoso, lento y susceptible a sesgos humanos. La falta de un modelo estandarizado genera inconsistencias en las valoraciones, afectando tanto a compradores como a instituciones financieras que basan sus decisiones de crédito en el valor del activo. Este proyecto aborda la necesidad de automatizar y objetivar el proceso de valoración mediante Machine Learning.

## 🎯 Objetivo del Proyecto
Construir un modelo supervisado de regresión capaz de estimar con precisión el precio de una vivienda a partir de sus características estructurales y de mercado, con el fin de:
- Reducir el **error de tasación manual** mediante predicción automatizada.
- Identificar las **variables con mayor influencia** en el precio final.
- Proveer una **base sólida y replicable** para la valoración automatizada de activos inmobiliarios.

## 🔍 Alcance del Análisis
- **Nivel de análisis:** Propiedad individual con variables estructurales y de mercado.
- **Datos incluidos:** Dataset del mercado inmobiliario con características como superficie, ubicación, número de habitaciones, año de construcción, entre otras.
- **Supuestos:** Se asume que las características estructurales y de localización son los principales determinantes del precio de mercado.

## 📊 Principales Insights del Análisis (EDA)
- **Correlaciones clave:** Se identificaron las variables con mayor correlación con el precio, destacando superficie habitable, calidad de construcción y ubicación geográfica.
- **Distribución asimétrica del precio:** El precio de venta presenta una distribución con sesgo positivo, lo que requirió transformaciones para mejorar el desempeño de los modelos lineales.
- **Valores atípicos:** Detección y tratamiento de propiedades con precios extremos que podrían distorsionar el entrenamiento del modelo.
- **Variables categóricas:** Identificación de atributos cualitativos con alto poder predictivo como el tipo de zona, calidad del vecindario y condición general de la propiedad.

## 🤖 Enfoque Analítico y Modelos
Se implementó un pipeline completo de modelado supervisado con comparación de múltiples algoritmos:

**Pipeline de datos:**
- Limpieza y tratamiento de valores nulos mediante imputación estratégica.
- Codificación de variables categóricas (One-Hot Encoding).
- Selección de características basada en análisis de correlaciones y relevancia.
- Normalización de variables numéricas para modelos sensibles a escala.

**Modelos evaluados y comparados:**
- **Linear Regression** — Modelo base para establecer benchmark de desempeño.
- **Ridge Regression** — Regularización L2 para controlar multicolinealidad.
- **Lasso Regression** — Regularización L1 con selección automática de variables.
- **Random Forest Regressor** — Modelo de ensamble para capturar relaciones no lineales.

## 📈 Métricas y Resultados
- **MAE (Error Medio Absoluto):** Evaluación del error promedio en unidades monetarias reales.
- **RMSE (Raíz del Error Cuadrático Medio):** Penalización de errores grandes para una estimación más conservadora.
- **R² (Coeficiente de Determinación):** Proporción de la varianza del precio explicada por el modelo.
- **Conclusión:** El pipeline estructurado logró reducir significativamente el error de tasación respecto al proceso manual, proporcionando valoraciones objetivas y replicables.

## 💼 Impacto en Decisiones de Negocio
- **Valoración Automatizada:** Reduce el tiempo y costo del proceso de tasación, habilitando evaluaciones masivas en tiempo real.
- **Soporte a Decisiones Crediticias:** Provee a instituciones financieras una estimación objetiva del valor del activo como respaldo para la aprobación de créditos hipotecarios.
- **Estrategia Comercial:** Permite a desarrolladores y agentes inmobiliarios fijar precios competitivos basados en evidencia cuantitativa.
- **Detección de Oportunidades:** Identifica propiedades subvaloradas o sobrevaloradas respecto al precio predicho por el modelo.

## 🛠️ Tecnologías y Herramientas Utilizadas
- **Lenguaje:** Python 3.x
- **ML Stack:** Scikit-Learn (Linear Regression, Ridge, Lasso, Random Forest)
- **Librerías:** Pandas, NumPy, Matplotlib, Seaborn
- **Entorno de trabajo:** Jupyter Notebook, GitHub

## 📂 Estructura del Repositorio
```
├── data/
│   └── housing_data.csv                    # Dataset del mercado inmobiliario
├── notebook/
│   └── predictive_housing_insights.ipynb   # Notebook principal del análisis
├── README.md                               # Documentación del proyecto
└── requirements.txt                        # Dependencias del entorno
```

## ▶️ Cómo Ejecutar el Proyecto
1. Clonar el repositorio:
   ```
   git clone https://github.com/DiegoTascon94/real-estate-price-prediction.git
   ```
2. Instalar dependencias:
   ```
   pip install -r requirements.txt
   ```
3. Abrir el análisis: Navegar a `/notebook` y ejecutar `predictive_housing_insights.ipynb`.

## 📝 Conclusiones
Este proyecto demuestra que la automatización del proceso de valoración inmobiliaria mediante Machine Learning no solo reduce el error humano, sino que también estandariza y escala la capacidad de tasación. La comparación sistemática de múltiples algoritmos garantiza que el modelo seleccionado sea el más adecuado para los datos disponibles, mientras que el análisis de importancia de variables provee insights accionables sobre los factores que realmente determinan el precio de una propiedad.

## 🔮 Próximos Pasos / Mejoras Futuras
- **Modelos Avanzados:** Implementar Gradient Boosting (XGBoost o LightGBM) para capturar patrones más complejos y mejorar la precisión predictiva.
- **Análisis Geoespacial:** Integrar datos de ubicación geográfica para capturar el efecto del vecindario y la proximidad a servicios en el precio.
- **API de Predicción:** Desarrollar un endpoint REST que permita consultar el precio estimado de una propiedad en tiempo real a partir de sus características.
- **Dashboard Interactivo:** Conectar el modelo a una herramienta de visualización (Power BI o Streamlit) para que agentes inmobiliarios puedan consultar valoraciones sin conocimientos técnicos.
