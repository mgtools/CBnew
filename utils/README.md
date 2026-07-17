# Utilities

Shared Python utilities and helper functions for the course.

## Structure

- `bio_helpers.py` - Common bioinformatics functions
- `ai_helpers.py` - AI/LLM integration helpers
- `visualization.py` - Plotting and visualization utilities
- `data_loaders.py` - Dataset loading and preprocessing

## Available Functions

### Bioinformatics Helpers
- Sequence manipulation
- Alignment functions
- Format conversion

### AI Helpers
- LLM prompt utilities
- Model loading functions
- Result parsing

## Usage

```python
from utils import bio_helpers, ai_helpers

# Example
sequence = bio_helpers.read_fasta('data.fasta')
ai_analysis = ai_helpers.analyze_with_llm(sequence)
```

## Contributing

Add new utilities as needed, but keep functions:
- Well-documented with docstrings
- Generic enough for multiple use cases
- Tested with example inputs
