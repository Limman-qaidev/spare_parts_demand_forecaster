# Spare Parts Demand Forecaster

Application for anticipating spare parts demand in repair workshops and generating replenishment recommendations based on repair history, inventory, and lead times.

## What it is

**Spare Parts Demand Forecaster** is a microproduct for workshops and aftersales operations that helps answer a simple operational question:

> Which parts should we replenish before they are needed?

The product combines a **predictive forecasting layer** with a **decision layer** that turns the prediction into alerts, priority levels, and suggested reorder quantities.

## Problem it solves

Many workshops manage spare parts reactively:

- parts are missing when a repair comes in,
- urgent orders have to be placed,
- customer waiting times increase,
- stock is not optimized,
- and planning depends too much on intuition or manual review.

The tool is designed to reduce that friction through a reproducible and explainable workflow.

## What the MVP does

The MVP allows the user to:

1. upload repair history, inventory, and lead times;
2. validate and transform the data;
3. predict future demand by part;
4. calculate stockout risk;
5. generate replenishment recommendations by priority;
6. display results in a visual app.

## Target users

- independent workshops with medium or high volume,
- workshop networks,
- spare parts distributors,
- aftersales operations.

## Value proposition

- reduces waiting times caused by missing parts,
- improves purchase planning,
- turns operational history into a decision-support tool,
- and shows applied AI in a clear and useful way.

## Repository scope

This repository is designed to serve **both** as:

- the development base for the product,
- a technical portfolio project,
- and a presentable asset for interviews or clients.

## Included documentation

- [Phase roadmap](docs/roadmap.md)
- [Initial prioritized backlog](docs/backlog.md)
- [High-level technical architecture](docs/architecture.md)
- [Functional product description](docs/product.md)
- [AI component description](docs/ai-component.md)
- [Proposed repository structure](docs/repository-structure.md)

## Recommended stack

- **Python 3.11+**
- **Streamlit** for the MVP frontend
- **pandas / numpy** for data handling
- **scikit-learn**, **XGBoost**, **LightGBM**, **CatBoost** for the predictive layer
- **SQLite** for initial persistence
- **Plotly** for visualisation
- **pytest** for testing
- **ruff / black** for code quality

## Architecture summary

- **Frontend**: Streamlit
- **Backend**: modular Python in the same repository
- **Predictive layer**: interchangeable boosting models
- **Decision layer**: decoupled risk and replenishment rules
- **Persistence**: SQLite
- **Visualisation**: Plotly

## Project status

This repository starts from a design and preparation phase. The intention is to evolve it in phases from a functional MVP to a polished portfolio version.

## Recommended first steps

1. Define and freeze the input data contract.
2. Prepare sample datasets for repairs, inventory, and lead times.
3. Implement the minimum pipeline:
   - ingestion,
   - validation,
   - feature engineering,
   - baseline model,
   - recommendation logic,
   - initial dashboard.
4. Add model comparison in the PoC:
   - HistGradientBoostingRegressor
   - XGBoost
   - LightGBM
   - CatBoost

## Portfolio narrative

This project should not be presented as a simple forecasting exercise, but as a **deployable operational tool** that combines:

- prediction,
- decision support,
- traceability,
- visualisation,
- and technical product design.

## Next key documents

The `docs/` folder contains the initial documentation base to start developing the project and using the repository as a portfolio asset from day one.
