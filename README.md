# SPARK Evaluation

## Overview

This repository contains all modules for evaluating and benchmarking humanoid robot performance using standardized metrics. It processes sensor data, runs analysis scripts, and generates comparative performance reports.

## Features

- Implements SPARK's seven standardized test categories
- Supports batch evaluation of multiple robot models
- Visual analytics for performance comparison
- Export of benchmark results (CSV, JSON, PDF)
- Statistical analysis and performance metrics
- Automated report generation

## Architecture

```
evaluation/
├── datasets/             # Sample motion and sensor datasets
├── protocols/            # Evaluation procedures and metric scripts
├── analysis/             # Performance computation and statistical tools
├── visualization/        # Plotting and dashboards (Matplotlib, Plotly)
├── reports/              # Generated evaluation summaries
├── config/               # Configuration files
├── tests/                # Unit and integration tests
└── main.py               # Entry point for evaluation pipeline
```

## Tech Stack

- **Language:** Python 3.11+
- **Libraries:** Pandas, Matplotlib, Plotly, NumPy, SciPy
- **Output Formats:** JSON, CSV, PDF
- **Visualization:** Matplotlib, Plotly, Seaborn

## Installation

```bash
# Clone the repository
git clone <repository-url>
cd spark_evaluation

# Install dependencies
pip install -r requirements.txt

# Run tests
python -m pytest tests/
```

## Usage

```python
from evaluation import protocols, analysis, visualization

# Example usage
evaluator = protocols.SPARKEvaluator()
results = evaluator.evaluate_robot(robot_data)
analysis.generate_report(results)
```

## Evaluation Categories

1. **Locomotion** - Walking, running, and movement patterns
2. **Manipulation** - Object handling and dexterity
3. **Balance** - Stability and equilibrium maintenance
4. **Coordination** - Multi-limb synchronization
5. **Adaptation** - Response to environmental changes
6. **Efficiency** - Energy consumption and optimization
7. **Reliability** - Consistency and error handling

## Integration

- Imports metric logic from `core/`
- Pulls simulation data from `simulator/`
- Publishes reports to `dashboard/` and via `api/`

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

## License

[Add license information here]
