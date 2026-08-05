# Reports

Esta carpeta está reservada para los outputs generados al ejecutar los notebooks del proyecto.

En GitHub se mantiene ligera para no subir archivos pesados o regenerables, pero después de ejecutar los notebooks deberían aparecer aquí tablas en `.csv`, versiones compatibles con Excel España y archivos `.xlsx`.

## Archivos esperados

### Notebook 1 — Dataset generation

- `data_dictionary_pricing.csv`

### Notebook 2 — Exploratory pricing analysis

- `route_summary_pricing.csv`
- `season_summary_pricing.csv`
- `monthly_summary_pricing.csv`
- `day_summary_pricing.csv`
- `booking_summary_pricing.csv`
- `competitor_summary_pricing.csv`
- `route_season_summary_pricing.csv`
- `route_diagnosis_pricing.csv`
- `executive_summary_notebook_02.md`

### Notebook 3 — Elasticity and break-even

- `elasticity_simple_by_route.csv`
- `elasticity_adjusted_by_route.csv`
- `elasticity_comparison_by_route.csv`
- `elasticity_route_season.csv`
- `pricing_scenario_simulation_by_route.csv`
- `pricing_best_scenarios_by_route.csv`
- `pricing_elasticity_route_diagnosis.csv`
- `executive_summary_notebook_03.md`

### Notebook 4 — Demand prediction model

- `demand_model_leaderboard.csv`
- `demand_model_predictions_test.csv`
- `demand_model_route_error_summary.csv`
- `demand_model_season_error_summary.csv`
- `demand_model_daily_predictions.csv`
- `demand_model_feature_importance.csv`
- `demand_model_route_diagnosis.csv`
- `executive_summary_notebook_04.md`

### Notebook 5 — Scenario simulation

- `pricing_simulation_scenario_config.csv`
- `pricing_simulation_detail.csv`
- `pricing_simulation_global_summary.csv`
- `pricing_simulation_route_scenario_summary.csv`
- `pricing_simulation_best_scenarios_by_route.csv`
- `pricing_simulation_best_balanced_by_route.csv`
- `pricing_simulation_route_recommendation.csv`
- `pricing_simulation_trip_recommendation.csv`
- `pricing_simulation_action_distribution.csv`
- `pricing_simulation_occupancy_risk_route.csv`
- `executive_summary_notebook_05.md`

### Notebook 6 — Pricing recommendation engine

- `pricing_recommender_scenarios.csv`
- `pricing_recommender_trip_recommendations.csv`
- `pricing_recommender_route_summary.csv`
- `pricing_recommender_action_distribution.csv`
- `pricing_recommender_route_action_distribution.csv`
- `pricing_recommender_high_priority.csv`
- `pricing_recommender_manual_review.csv`
- `executive_summary_notebook_06.md`

### Notebook 7 — Executive dashboard

- `dashboard_executive_kpis.csv`
- `dashboard_route_table.csv`
- `dashboard_top_recommendations.csv`
- `dashboard_manual_review_table.csv`
- `dashboard_loaded_status.csv`
- `final_executive_summary_project_03_pricing.md`

## Nota de portfolio

Los archivos de esta carpeta son outputs reproducibles. Para mantener el repositorio limpio, se recomienda subir solo:

1. Resúmenes ejecutivos `.md`.
2. Tablas finales clave.
3. Capturas del dashboard en `assets/screenshots/`.
4. No subir todos los CSV intermedios si hacen el repositorio demasiado pesado.
