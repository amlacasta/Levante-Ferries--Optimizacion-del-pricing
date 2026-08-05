# Data Dictionary — Levante Ferries Pricing Dataset

| Column | Description |
|---|---|
| `trip_id` | Unique trip identifier |
| `trip_date` | Trip date |
| `departure_datetime` | Departure datetime |
| `year` | Year |
| `month` | Month |
| `week` | ISO week |
| `day_of_week` | Day of week |
| `is_weekend` | Weekend flag |
| `season` | Low, Shoulder or High season |
| `high_season_flag` | High season indicator |
| `route` | Ferry route |
| `origin` | Origin port |
| `destination` | Destination port |
| `route_type` | Route category |
| `vessel_type` | Vessel type |
| `departure_hour` | Departure hour |
| `capacity` | Passenger capacity |
| `base_price` | Base route price |
| `avg_ticket_price` | Average ticket price |
| `competitor_price` | Estimated competitor price |
| `price_index_vs_competitor` | Price divided by competitor price |
| `route_elasticity` | Simulated price-demand elasticity by route |
| `days_before_departure` | Booking anticipation |
| `booking_window` | Early, Medium, Short or Last minute |
| `weather_score` | Simulated weather score |
| `event_flag` | Event indicator |
| `expected_demand` | Expected demand before capacity cap |
| `tickets_sold` | Tickets sold |
| `occupancy_rate` | Tickets sold divided by capacity |
| `revenue` | Ticket revenue |
| `fixed_operational_cost` | Fixed operational cost per trip |
| `variable_cost_per_passenger` | Variable cost per passenger |
| `total_operational_cost` | Total trip cost |
| `margin` | Revenue minus total cost |
| `margin_pct` | Margin divided by revenue |
| `demand_level` | Demand classification |
| `pricing_opportunity` | Initial pricing opportunity label |
| `trip_feature` | Combined business feature for analysis |
