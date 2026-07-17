# Setup & Environment Configuration

This directory contains configuration and setup files for the course.

## Files

- `requirements.txt` - Python package dependencies
- `environment.yml` - Conda environment specification
- `.env.example` - Environment variables template
- `setup.sh` - Automated setup script (Unix/Linux/Mac)
- `setup.bat` - Automated setup script (Windows)

## Quick Setup

### Using pip

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Using conda

```bash
conda env create -f environment.yml
conda activate cbnew
```

### API Configuration

1. Copy `.env.example` to `.env`
2. Add your API keys:
   - OpenAI API key (for GPT models)
   - Anthropic API key (for Claude)
   - Other service credentials as needed
3. Never commit `.env` to version control

## Verification

Run tests to verify setup:

```bash
python -m pytest tests/
```

## Troubleshooting

See [../docs/guides/setup-guide.md](../docs/guides/setup-guide.md) for detailed troubleshooting.
