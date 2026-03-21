# Proposed repository structure

```text
spare-parts-demand-forecaster/
│
├── app/
│   ├── ui/                                         # Contains only the visual and iteractoin layer
│   │   ├── pages/
│   │   │   ├── upload.py
│   │   │   ├── dashboard.py
│   │   │   ├── forecasts.py
│   │   │   ├── recommendations.py
│   │   │   └── settings.py
│   │   ├── components/
│   │   │   ├── charts.py
│   │   │   ├── tables.py
│   │   │   └── cards.py
│   │   └── main.py
│   │
│   ├── core/
│   │   ├── config.py
│   │   ├── constants.py
│   │   └── logger.py
│   │
│   ├── data/                                       # Groups ingestion, validation, cleaning, and feature building
│   │   ├── ingestion.py
│   │   ├── validation.py
│   │   ├── cleaning.py
│   │   ├── feature_engineering.py
│   │   └── repository.py
│   │
│   ├── models/                                     # Contains the predictive layer and abstracts the concrete models
│   │   ├── base.py
│   │   ├── hist_gb.py
│   │   ├── xgboost_model.py
│   │   ├── lightgbm_model.py
│   │   ├── catboost_model.py
│   │   ├── registry.py
│   │   └── inference.py
│   │
│   ├── decision/                                   # Contains the business logic that turns forecasts into recommendations.
│   │   ├── risk_scoring.py
│   │   ├── reorder_policy.py
│   │   └── explanation.py
│   │
│   ├── services/                                   # Orchestrates modules and prepares results consumable by the UI.
│   │   ├── training_service.py
│   │   ├── forecast_service.py
│   │   ├── recommendation_service.py
│   │   └── dashboard_service.py
│   │
│   ├── storage/                                    # Centralizes persistence and database access.
│   │   ├── db.py
│   │   ├── models.py
│   │   └── migrations/
│   │
│   └── utils/
│       ├── dates.py
│       ├── metrics.py
│       └── helpers.py
│
├── data_samples/                                  # Allows the demo to run without depending on external data.
│   ├── repairs_sample.csv
│   ├── inventory_sample.csv
│   ├── lead_times_sample.csv
│   └── README.md
│
├── notebooks/                                     # Experimentation space, not the product core.
│   ├── 01_exploration.ipynb
│   ├── 02_model_comparison.ipynb
│   └── 03_decision_logic_tests.ipynb
│
├── models_artifacts/
│   ├── histgb/
│   ├── xgboost/
│   ├── lightgbm/
│   └── catboost/
│
├── tests/
│   ├── test_validation.py
│   ├── test_features.py
│   ├── test_forecasting.py
│   ├── test_decision_logic.py
│   └── test_services.py
│
├── docs/
│   └── repository-structure.md
│
├── .env.example
├── .gitignore
├── pyproject.toml
├── requirements.txt
└── README.md
```
