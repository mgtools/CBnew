# Images & Assets Guide

This directory stores supporting files for Jupyter notebooks.

## Structure

```
assets/
├── images/          # Figures, diagrams, screenshots
│   ├── workflow_diagram.png
│   ├── plddt_example.png
│   └── structure_viz.png
└── data/            # Sample datasets
    ├── example_sequences.fasta
    ├── sample_prediction.json
    └── test_data.csv
```

## Adding Your Workflow Diagram

### Step 1: Create/Prepare Your Image
Your protein structure prediction workflow diagram should ideally show:
- Step 1: Protein Selection (database queries)
- Step 2: Sequence Preparation (validation)
- Step 3: Structure Prediction (AlphaFold/AlphaSense)
- Step 4: Analysis (quality metrics)
- Step 5: Interpretation (AI-assisted insights)

### Step 2: Save as Image File
- **Format:** PNG, JPG, or SVG
- **Size:** 1000-2000 pixels wide recommended
- **Quality:** 150-300 DPI for clarity

### Step 3: Place in `images/` Folder
```bash
cp your_diagram.png notebooks/assets/images/workflow_diagram.png
```

### Step 4: Reference in Notebook
```markdown
![Protein Structure Prediction Workflow](assets/images/workflow_diagram.png)
```

## Image Types & Recommendations

### Workflow Diagrams
- **Tool:** Draw.io, Lucidchart, Adobe Illustrator
- **Format:** PNG or SVG (SVG scales better)
- **Contains:** Steps, arrows, decision points, outputs
- **Example:** Complete pipeline from protein selection to interpretation

### Screenshots
- **Tool:** Screenshot utility (Mac: Cmd+Shift+4, Windows: Win+Shift+S)
- **Format:** PNG (lossless)
- **Use:** Show database interfaces, AlphaFold results

### Plots & Graphs
- **Tool:** Matplotlib, Seaborn, or plotting software
- **Format:** PNG or PDF
- **Use:** Confidence scores, alignments, structures

### 3D Structures
- **Tool:** PyMOL, Chimera, or Mol*
- **Format:** PNG or SVG (with transparency)
- **Use:** Protein structure examples, comparison figures

## Editing Existing Images

### If you want to edit workflow_diagram.png:
1. Open in image editor (Photoshop, GIMP, etc.)
2. Make changes
3. Save/Export to PNG
4. Replace the file in this folder

### Version Control
If making significant changes, consider naming with versions:
```
workflow_diagram_v1.png
workflow_diagram_v2.png
```

## Image File Size Tips

Keep file sizes reasonable for git repositories:
- PNG: < 500 KB per image
- JPG: < 300 KB per image
- SVG: Often < 100 KB and scales perfectly

**Compression tools:**
- Online: TinyPNG.com, Compressor.io
- Command line: `pngquant`, `imagemin`
- Mac: `sips -Z 800 image.png`

## Placeholder Images

The notebook currently uses a placeholder:
```markdown
![Protein Structure Prediction Workflow](assets/images/workflow_diagram.png)
```

Once you add your `workflow_diagram.png` file here, it will automatically display in the notebook.

## Data Files

### Sample Sequences (FASTA format)
```fasta
>HUMAN_INSULIN
MALWMRLLPLLALTALPWWAKEAVTPEEAOLQCGSQSLYQLENYCN
>MOUSE_INSULIN
MALWMRLLPLLALTALPWWAKEAVTPEEAOLQCGSQSLYQLENYCN
```

### Prediction Results (JSON format)
```json
{
  "protein_id": "P01308",
  "sequence": "MALWMRLLPLLALTALPWWAKEAVTPEEAOLQCGSQSLYQLENYCN",
  "plddt_scores": [0.5, 0.75, 0.8, ...],
  "mean_confidence": 0.75
}
```

## Image Organization Best Practices

1. **Descriptive names:** `workflow_diagram.png` not `image1.png`
2. **Consistent format:** Use PNG for most images
3. **Organized structure:** Keep images/ and data/ separate
4. **Version tracking:** Mark major revisions if needed
5. **Documentation:** Note image source/author when relevant

## Adding Images to Git

```bash
# Add image to git
git add notebooks/assets/images/workflow_diagram.png

# Commit
git commit -m "Add protein structure prediction workflow diagram"

# Push
git push
```

---

**Created:** July 17, 2026  
**Purpose:** Central hub for notebook supporting files
