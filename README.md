# SPARK Evaluation

## Overview

This repository contains all modules for evaluating and benchmarking humanoid robot performance using standardized metrics.  
It processes sensor data, runs analysis scripts, and generates comparative performance reports.

## Features

- Implements SPARK’s seven standardized test categories
- Supports batch evaluation of multiple robot models
- Visual analytics for performance comparison
- Export of benchmark results (CSV, JSON, PDF)

## Architecture

evaluation/
├── datasets/ # Sample motion and sensor datasets
├── protocols/ # Evaluation procedures and metric scripts
├── analysis/ # Performance computation and statistical tools
├── visualization/ # Plotting and dashboards (Matplotlib, Plotly)
├── reports/ # Generated evaluation summaries
└── main.py

## Tech Stack

- **Python 3.11+**
- **Libraries:** Pandas, Matplotlib, Plotly, NumPy, SciPy
- **Output Formats:** JSON, CSV, PDF

## Integration

- Imports metric logic from `core/`
- Pulls simulation data from `simulator/`
- Publishes reports to `dashboard/` and via `api/`
