# Setup Process Documentation

## Project Overview

**Repository:** CBnew  
**Purpose:** AI-Enhanced Computational Biology Course  
**Date:** July 17, 2026  
**Owner:** mgtools

### Initial Vision

A redesigned computational biology course that leverages:
- New AI models for various biological problems
- AI-assisted programming to help students learn coding
- Integration of LLMs (Claude, GPT) for biological analysis
- Interactive Jupyter notebooks with hands-on examples

---

## Setup Prompts & Commands Used

### 1. Initial Request
```
"I is a repo for computational biology course that i redesigned to leverage 
what AI can offer, through the new AI models for various biological problems, 
and programming with AI assists."
```

### 2. Directory Structure Setup Request
```
"set up the directory structure"
```

---

## Directory Structure Created

### Root-Level Directories

```
CBnew/
├── modules/                    # Organized course content by topic
├── assignments/                # Student assignments and projects
├── notebooks/                  # Jupyter notebooks for interactive learning
├── datasets/                   # Data files used in course
├── ai-tools/                   # AI integrations and configurations
├── utils/                      # Shared utility functions and helpers
├── docs/                       # Documentation and guides
├── setup/                      # Environment configuration
└── .gitignore                  # Git configuration
```

### Module Subdirectories

Four core computational biology modules were created:

```
modules/
├── 01-sequence-analysis/       # DNA/RNA sequence analysis with AI
├── 02-protein-structure/       # Protein folding & structure prediction
├── 03-phylogenetics/          # Evolutionary analysis with AI
└── 04-genomics/               # Large-scale genomic data analysis
```

### AI Tools Organization

```
ai-tools/
├── llm-prompts/               # Optimized LLM prompts for biology tasks
├── ml-models/                 # ML model configurations and integrations
├── integrations/              # API clients for Claude, GPT, etc.
└── README.md                  # Guide to AI tools
```

### Data Management

```
datasets/
├── sample-data/               # Pre-processed, ready-to-use datasets
├── raw/                       # Original datasets requiring preprocessing
└── README.md                  # Dataset documentation
```

### Documentation Structure

```
docs/
├── guides/                    # Setup, integration, best practices guides
├── api-references/           # API documentation
└── README.md                 # Documentation index
```

### Setup & Configuration

```
setup/
├── requirements.txt           # Python package dependencies
├── environment.yml            # Conda environment specification
├── .env.example              # API key template
└── README.md                 # Setup instructions
```

---

## Files Created

### Configuration Files

#### 1. `.gitignore`
**Purpose:** Prevent committing sensitive and unnecessary files

**Excluded:**
- Python cache files (`__pycache__/`, `*.pyc`)
- Environment files (`.env`, `.venv/`)
- IDE settings (`.vscode/`, `.idea/`)
- Data files (`*.csv`, `*.pkl`, `*.h5`)
- Jupyter checkpoints
- Build artifacts

#### 2. `setup/requirements.txt`
**Purpose:** Python package management

**Included Dependencies:**
- `biopython` - Bioinformatics tools
- `jupyter`, `jupyterlab` - Notebook environment
- `numpy`, `pandas` - Data manipulation
- `matplotlib`, `seaborn` - Visualization
- `scipy`, `scikit-learn` - Scientific computing & ML
- `requests` - HTTP client
- `python-dotenv` - Environment variable management

#### 3. `setup/.env.example`
**Purpose:** Template for API credentials

**Configured for:**
- OpenAI API key (GPT models)
- Anthropic API key (Claude)
- Database credentials (optional)
- Course configuration options

**Usage:** Copy to `.env` and fill with actual credentials (never commit `.env`)

### Documentation Templates

#### 4. `README.md` (Root)
**Purpose:** Main project documentation

**Contents:**
- Project description and key features
- Directory structure overview
- Installation instructions
- Course module descriptions
- Resource links

**Key Features Highlighted:**
- AI-Powered Learning
- Programming-First Approach
- Comprehensive Resources

#### 5. `modules/MODULE_TEMPLATE.md`
**Purpose:** Template for course modules

**Sections:**
- Module title and overview
- Learning objectives
- Topics covered
- File structure
- AI integration points
- Key takeaways
- Getting started guide
- Resources

#### 6. `assignments/ASSIGNMENT_TEMPLATE.md`
**Purpose:** Standardized assignment structure

**Sections:**
- Assignment overview
- Learning objectives
- Requirements checklist
- Task breakdown
- Deliverables
- Resources and references
- Submission guidelines

#### 7. Directory READMEs

Created README files for:
- `ai-tools/` - AI services and model documentation
- `datasets/` - Dataset inventory and usage guide
- `utils/` - Utility functions reference
- `docs/` - Documentation index
- `setup/` - Environment setup instructions

---

## Design Rationale

### Module Organization
- **Numbered prefixes** (01-, 02-, etc.) ensure alphabetical sorting
- **Descriptive names** make module purpose clear at a glance
- **Self-contained** - Each module has its own resources

### AI Tools Separation
- **llm-prompts/** - Centralize LLM prompt engineering
- **ml-models/** - Organize pre-trained and custom models
- **integrations/** - Standardize API client code
- **Rationale:** Easy to add new AI services without cluttering course content

### Dataset Management
- **sample-data/** - Preprocessed for quick examples
- **raw/** - Original data preserved for reproducibility
- **Rationale:** Students learn data cleaning while having working examples

### Documentation Strategy
- **guides/** - How-to and setup documentation
- **api-references/** - API specification documentation
- **Rationale:** Separate learning resources from reference material

### Setup Configuration
- **requirements.txt** - Standard Python packaging
- **.env.example** - Secrets management best practice
- **README.md** - Clear setup instructions
- **Rationale:** Enables quick environment reproducibility

---

## Configuration Details

### Python Environment

**Minimum Python Version:** 3.10+

**Key Package Groups:**
1. **Bioinformatics**: Biopython (sequence analysis, alignment)
2. **Data Science**: NumPy, Pandas, SciPy, Scikit-learn
3. **Notebooks**: Jupyter, JupyterLab
4. **Visualization**: Matplotlib, Seaborn
5. **Utilities**: Requests, python-dotenv

### API Configuration

Environment variables configured for:
- **OpenAI** - GPT-4, GPT-3.5 models
- **Anthropic** - Claude LLM
- **Optional** - Database, custom services

---

## Workflow: Using This Structure

### For Course Instructors

1. **Create a new module**
   - Copy `modules/MODULE_TEMPLATE.md` to `modules/NN-topic-name/`
   - Create corresponding Jupyter notebook
   - Add assignment to `assignments/`

2. **Add course data**
   - Place raw data in `datasets/raw/`
   - Preprocess to `datasets/sample-data/`
   - Document in `datasets/README.md`

3. **Integrate AI tools**
   - Store LLM prompts in `ai-tools/llm-prompts/`
   - Configure models in `ai-tools/ml-models/`
   - Add integration code to `ai-tools/integrations/`

### For Students

1. **Setup environment**
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r setup/requirements.txt
   ```

2. **Configure API keys**
   ```bash
   cp setup/.env.example .env
   # Edit .env with actual credentials
   ```

3. **Work through modules**
   - Read module README and lecture notes
   - Complete Jupyter notebook examples
   - Work on assignments
   - Review resources for deeper learning

---

## Next Steps & Recommendations

### Immediate (Phase 1)
- [ ] Populate `modules/` with actual course content
- [ ] Create Jupyter notebook templates
- [ ] Add sample datasets to `datasets/sample-data/`
- [ ] Write setup and AI integration guides

### Short-term (Phase 2)
- [ ] Create LLM prompt library in `ai-tools/llm-prompts/`
- [ ] Set up ML model configurations
- [ ] Build utility functions in `utils/`
- [ ] Create example assignments

### Medium-term (Phase 3)
- [ ] Integrate API clients for common services
- [ ] Add example notebooks demonstrating AI workflows
- [ ] Build student assessment tools
- [ ] Create instructor guides

### Long-term (Phase 4)
- [ ] Student submission system
- [ ] Automated grading with AI
- [ ] Feedback generation using LLMs
- [ ] Course analytics and tracking

---

## Tools & Processes Used

### Directory Creation
- Created 11 main directories
- Created 8 subdirectories for modules and data organization
- Total: 19+ organized directories

### File Generation
- **Configuration files**: 3 (requirements.txt, .env.example, .gitignore)
- **Documentation files**: 9 (READMEs and templates)
- **Total**: 12 files created

### Documentation Coverage
- Root-level README with full project overview
- Directory-specific READMEs with usage guides
- Template files for modules and assignments
- Configuration templates with comments

---

## File Manifest

| Path | Type | Purpose |
|------|------|---------|
| README.md | Doc | Main project README |
| .gitignore | Config | Git ignore rules |
| setup/requirements.txt | Config | Python dependencies |
| setup/.env.example | Config | API credentials template |
| setup/README.md | Doc | Setup instructions |
| modules/MODULE_TEMPLATE.md | Template | Module structure template |
| assignments/ASSIGNMENT_TEMPLATE.md | Template | Assignment structure template |
| ai-tools/README.md | Doc | AI tools guide |
| datasets/README.md | Doc | Dataset documentation |
| utils/README.md | Doc | Utility functions guide |
| docs/README.md | Doc | Documentation index |

---

## Commit Information

This setup was designed to be initialized with:
```bash
git add .
git commit -m "Initial project structure for AI-enhanced computational biology course"
```

---

## Contact & Support

For questions about:
- **Course content**: See `docs/guides/`
- **AI integration**: See `ai-tools/README.md`
- **Setup issues**: See `setup/README.md`
- **Development**: See `docs/guides/programming-best-practices.md` (to be created)

