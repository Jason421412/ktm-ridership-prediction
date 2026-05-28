# Project Decisions

## Notebook First

This repository is currently notebook-first because the main goal is exploratory ML workflow documentation: loading data, checking patterns, engineering features, comparing models, and reviewing outputs.

Future versions should add scripts once the workflow stabilizes.

## Data Not Committed

The raw dataset is not committed because the source, license, size, and redistribution permissions need to be confirmed. This is the safer choice for a public portfolio repository.

## Model Comparison

The project is framed around regression model comparison rather than one claimed best model. This avoids overstating results before exported metrics and validation methodology are tracked.

## Evaluation Caution

Ridership data has time structure. Random train/test splits may leak future patterns into training. A time-based split or backtesting workflow should be preferred for serious evaluation.

## Portfolio Boundary

This repository demonstrates ML/data analytics workflow thinking. It should not claim production forecasting readiness until it has:

- clear dataset provenance
- reproducible scripts
- exported metrics
- leakage-aware validation
- documented model limitations
