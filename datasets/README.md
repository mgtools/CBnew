# Datasets

This directory contains datasets used throughout the course.

## Structure

- **sample-data/**: Pre-processed, ready-to-use datasets for examples and assignments
- **raw/**: Original datasets (may require preprocessing)

## Available Datasets

| Name | Type | Size | Source | Module |
|------|------|------|--------|--------|
| [Add dataset info] | Sequence | [Size] | [Source] | Sequence Analysis |
| [Add dataset info] | Structure | [Size] | [Source] | Protein Structure |

## Usage

All datasets should be referenced with relative paths from the repository root:

```python
import pandas as pd

# Example
data = pd.read_csv('datasets/sample-data/example.csv')
```

## Data Privacy & Attribution

- Always check the LICENSE and ATTRIBUTION files in each dataset folder
- Provide proper citations when publishing results
- Follow institutional and funder data policies

## Adding New Datasets

1. Place raw data in `raw/`
2. Add preprocessing scripts in corresponding module
3. Place cleaned data in `sample-data/`
4. Document in this README with source and license info
