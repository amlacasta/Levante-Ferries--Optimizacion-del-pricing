# Levante Ferries — Dynamic Pricing & Revenue Optimization

## Proyecto de portfolio · Business Analytics / Data Science / Revenue Management

Este proyecto construye un sistema analítico completo para apoyar decisiones de pricing en una compañía ficticia de ferries: **Levante Ferries**.

El objetivo no es crear un sistema automático que suba o baje precios sin control, sino una capa de apoyo a decisión que combine:

- Demanda esperada.
- Elasticidad precio-demanda.
- Ocupación.
- Capacidad.
- Costes operativos.
- Margen.
- Precio frente al competidor.
- Punto de equilibrio.
- Simulación de escenarios.
- Recomendaciones explicables.

---

## 1. Problema de negocio

En una compañía de ferries, cada salida tiene una capacidad limitada. Una vez que el barco zarpa, las plazas vacías no se pueden recuperar.

Una decisión de pricing incorrecta puede provocar:

- Alta ocupación, pero margen débil.
- Precio demasiado alto y caída de demanda.
- Promociones que aumentan tickets, pero destruyen rentabilidad.
- Rutas con buena demanda, pero bajo margen.
- Falta de claridad sobre qué rutas deben subir, mantener o promocionar.

Este proyecto responde a una pregunta central:

> ¿Cómo podemos recomendar precios de forma explicable, equilibrando revenue, margen, ocupación, elasticidad y competencia?

---

## 2. Objetivos del proyecto

El proyecto tiene los siguientes objetivos:

1. Construir un dataset sintético realista de rutas de ferry.
2. Analizar pricing, demanda, ocupación, revenue y margen.
3. Estimar elasticidad precio-demanda por ruta.
4. Calcular puntos de equilibrio y precios mínimos rentables.
5. Entrenar un modelo predictivo de demanda.
6. Simular escenarios de cambio de precio.
7. Crear un recomendador formal de pricing.
8. Generar herramientas interactivas.
9. Construir un dashboard ejecutivo final.
10. Documentar el proyecto como portfolio profesional.

---

## 3. Dataset

Cada fila representa una salida concreta de ferry.

Variables principales:

| Grupo | Variables |
|---|---|
| Tiempo | `trip_date`, `departure_datetime`, `month`, `week`, `day_of_week`, `season`, `departure_hour` |
| Ruta | `route`, `origin`, `destination`, `route_type`, `vessel_type`, `capacity` |
| Pricing | `base_price`, `avg_ticket_price`, `competitor_price`, `price_index_vs_competitor` |
| Demanda | `expected_demand`, `tickets_sold`, `occupancy_rate`, `demand_level` |
| Costes | `fixed_operational_cost`, `variable_cost_per_passenger`, `total_operational_cost` |
| Finanzas | `revenue`, `margin`, `margin_pct` |
| Analítica | `route_elasticity`, `pricing_opportunity`, `trip_feature` |

Los datos son **sintéticos** y se han creado con lógica de negocio para evitar el uso de información confidencial.

---

## 4. Arquitectura del proyecto

```text
3 Pricing/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_dataset_generation_pricing.ipynb
│   ├── 02_exploratory_pricing_analysis.ipynb
│   ├── 03_price_elasticity_analysis_with_break_even_tool_v2_fixed.ipynb
│   ├── 04_demand_prediction_model_corrected_path.ipynb
│   ├── 05_advanced_pricing_scenario_simulation_with_interactive_simulators.ipynb
│   ├── 06_formal_pricing_recommendation_engine.ipynb
│   └── 07_executive_pricing_dashboard.ipynb
│
├── reports/
│   ├── executive_summary_notebook_*.md
│   ├── pricing_recommender_*.csv
│   ├── dashboard_*.csv
│   └── *.xlsx
│
├── images/
│   └── *.png
│
├── models/
│   └── demand_prediction_model_*.joblib
│
├── dashboard/
│   ├── pricing_interactive_simulator.html
│   ├── break_even_pricing_decision_tool.html
│   ├── pricing_recommendation_explorer.html
│   └── executive_pricing_dashboard.html
│
└── README.md
```

---

## 5. Notebooks

### Notebook 1 — Dataset generation

Crea el dataset sintético con lógica de negocio:

- Rutas.
- Temporadas.
- Precios.
- Demanda.
- Costes.
- Margen.
- Oportunidades de pricing.
- Diccionario de datos.

### Notebook 2 — Exploratory pricing analysis

Analiza:

- Revenue por ruta.
- Margen por ruta.
- Ocupación por ruta.
- Precio por temporada.
- Comparación con competidor.
- Diagnóstico inicial de pricing.

### Notebook 3 — Price elasticity & break-even analysis

Estima:

- Elasticidad simple.
- Elasticidad ajustada.
- Elasticidad por ruta y temporada.
- Escenarios de precio.
- Punto de equilibrio.
- Precio mínimo rentable.

Incluye una herramienta interactiva:

```text
Break-even Pricing Decision Tool
```

### Notebook 4 — Demand prediction model

Entrena modelos para predecir `tickets_sold`:

- Baseline.
- Linear Regression.
- Ridge Regression.
- Random Forest.
- Gradient Boosting.

Métricas:

- MAE.
- RMSE.
- R².
- MAPE.

### Notebook 5 — Advanced pricing scenario simulation

Simula escenarios de precio entre -20% y +20%.

Calcula:

- Demanda simulada.
- Tickets simulados.
- Ocupación.
- Revenue.
- Margen.
- Revenue uplift.
- Margin uplift.
- Riesgo de ocupación.

Incluye simuladores interactivos en Colab y HTML.

### Notebook 6 — Formal pricing recommendation engine

Construye el recomendador formal.

Acciones posibles:

- `Increase price`
- `Promotional action`
- `Maintain / monitor`
- `Margin review`
- `Capacity / premium review`
- `Manual review`

Cada recomendación incluye:

- Precio recomendado.
- Cambio de precio.
- Score.
- Nivel de confianza.
- Explicación de negocio.

### Notebook 7 — Executive pricing dashboard

Construye el dashboard final:

- KPIs ejecutivos.
- Revenue y margen.
- Uplift estimado.
- Acciones recomendadas.
- Resumen por ruta.
- Top recomendaciones.
- Herramientas interactivas enlazadas.

---

## 6. KPIs principales

| Categoría | KPIs |
|---|---|
| Comercial | Revenue, precio medio, price index vs competitor |
| Demanda | Tickets, ocupación, demanda esperada |
| Rentabilidad | Margen, margen %, coste operativo |
| Pricing | Elasticidad, cambio recomendado, acción recomendada |
| Simulación | Revenue uplift, margin uplift, ocupación simulada |
| Modelo | MAE, RMSE, R², MAPE |
| Recomendador | Score, confianza, revisión manual |

---

## 7. Lógica del precio recomendado

El precio recomendado se obtiene mediante simulación de escenarios.

Para cada viaje:

1. Se toma el precio actual.
2. Se prueban escenarios de cambio de precio.
3. Se estima la nueva demanda usando elasticidad.
4. Se limita la demanda por capacidad.
5. Se calcula revenue.
6. Se calcula coste.
7. Se calcula margen.
8. Se calcula un score de negocio.
9. Se elige el escenario con mayor score.

La fórmula conceptual de demanda simulada es:

```text
demanda simulada =
demanda base × (precio recomendado / precio actual) ^ elasticidad
```

El score combina:

```text
30% revenue uplift
35% margin uplift
20% ocupación saludable
15% posición competitiva
- penalizaciones por riesgo
```

---

## 8. Herramientas interactivas

El proyecto incluye varias herramientas HTML:

### Pricing Interactive Simulator

Permite simular:

- Ruta.
- Cambio de precio.
- Demanda externa.
- Shock de coste.

### Break-even Pricing Decision Tool

Permite calcular:

- Ocupación de equilibrio.
- Pasajeros mínimos.
- Precio mínimo.
- Margen por salida.

### Pricing Recommendation Explorer

Permite filtrar recomendaciones por:

- Ruta.
- Temporada.
- Acción.
- Confianza.

### Executive Pricing Dashboard

Dashboard final con KPIs, rutas, acciones, recomendaciones y herramientas.

---

## 9. Stack técnico

- Python.
- Pandas.
- NumPy.
- Matplotlib.
- Seaborn.
- Scikit-learn.
- Joblib.
- Openpyxl.
- HTML.
- CSS.
- JavaScript.
- Google Colab.
- Google Drive.
- Excel.
- GitHub.

---

## 10. Principales aprendizajes

Este proyecto demuestra que el pricing dinámico no debe basarse solo en subir precios.

Una buena decisión de pricing necesita equilibrar:

- Demanda.
- Ocupación.
- Margen.
- Elasticidad.
- Competencia.
- Costes.
- Capacidad.
- Riesgo.

La conclusión principal es:

> Revenue Management no consiste en vender más caro, sino en vender mejor.

---

## 11. Limitaciones

Este proyecto tiene algunas limitaciones intencionadas:

- Los datos son sintéticos.
- No se usan datos reales de ninguna empresa.
- No se modelan segmentos de cliente.
- No se incluyen vehículos, camarotes o servicios auxiliares.
- No se incorpora competencia real en tiempo real.
- No se optimiza con algoritmos matemáticos avanzados.
- No se automatiza la aplicación real de precios.

---

## 12. Mejoras futuras

Posibles ampliaciones:

- Segmentación de clientes.
- Forecasting temporal avanzado.
- Optimización matemática de precios.
- App en Streamlit.
- Dashboard Power BI.
- Eventos reales.
- Climatología real.
- Scraping autorizado de precios competidores.
- Modelos XGBoost / LightGBM.
- Optimización por canal de venta.
- Análisis de cancelaciones y no-shows.

---

## 13. Cómo explicar este proyecto en entrevista

Una forma clara de explicarlo:

> Construí un proyecto completo de revenue management aplicado a rutas de ferry. Primero generé un dataset sintético con lógica de negocio, después analicé revenue, ocupación y margen, estimé elasticidad precio-demanda, entrené un modelo predictivo de demanda, simulé escenarios de precio y finalmente creé un recomendador formal explicable. El resultado final es un dashboard ejecutivo que permite ver qué rutas deberían subir precio, mantener, promocionar o revisar manualmente.

---

## 14. Autor

Proyecto desarrollado como parte de un portfolio profesional de Business Analytics, Data Science e Inteligencia Artificial aplicada a negocio.

**Enfoque profesional:** Dirección + Datos + IA aplicada a operaciones, pricing y toma de decisiones.
