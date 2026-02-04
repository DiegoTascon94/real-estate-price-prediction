# 🎟️ Showz: Optimización de Marketing y Rentabilidad de Clientes

## 📊 Descripción del Proyecto
**Showz** es una plataforma de venta de entradas para eventos. El departamento de marketing busca optimizar sus gastos publicitarios y comprender mejor el comportamiento de los usuarios. En este proyecto, analizo la efectividad de las campañas y la rentabilidad de los clientes adquiridos a través de distintas fuentes de tráfico mediante el cálculo de métricas de negocio avanzadas.

## 🚀 Objetivos Principales
1.  **Análisis de Comportamiento:** Evaluar el engagement mediante métricas de usuarios activos (**DAU, WAU, MAU**).
2.  **Conversión y Retención:** Determinar cuánto tiempo tardan los usuarios en convertir y cómo es su retención por cohortes.
3.  **Métricas Financieras:** Calcular el **Ticket Promedio**, **LTV** (Lifetime Value) y **CAC** (Costo de Adquisición).
4.  **ROMI (Return on Marketing Investment):** Identificar qué canales de marketing generan mayor retorno y recomendar la asignación eficiente del presupuesto.

## 📂 Estructura del Repositorio
* `predictive_housing_insights.ipynb`: Notebook principal con el análisis de Showz.
* `visits_log_us.csv`: Datos de sesiones, dispositivos y fuentes de origen.
* `orders_log_us.csv`: Registro de pedidos y facturación (Revenue).
* `costs_us.csv`: Detalle de gastos de marketing por fuente de adquisición.
* `requirements.txt`: Librerías necesarias para replicar el análisis.

## 🛠️ Tecnologías Utilizadas
* **Python 3.x**
* **Pandas:** Manipulación y limpieza de datos (Conversión a `datetime`, `to_period`, agrupaciones).
* **Matplotlib & Seaborn:** Visualización de tendencias temporales y análisis de cohortes (Heatmaps).

## 📈 Flujo de Trabajo
1.  **Preparación de Datos:** Conversión de tipos de datos, limpieza de nombres de columnas y manejo de periodos temporales.
2.  **Exploración de Métricas de Producto:** Cálculo de la frecuencia de uso de la plataforma.
3.  **Análisis de Ventas:** Evolución del volumen de pedidos y el ingreso promedio.
4.  **Evaluación de Marketing:** Cálculo de costos de adquisición por fuente y análisis de rentabilidad (ROMI) para identificar los canales más eficientes.

## 📝 Conclusiones
El análisis permite identificar los canales de adquisición con el menor tiempo de recuperación de inversión (Payback) y aquellos donde el LTV justifica un aumento en el gasto publicitario. Esto proporciona una base sólida para que el departamento de marketing de **Showz** tome decisiones basadas en datos.
