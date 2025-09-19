# RNA Folding Pipeline – Demo Notebook

This branch contains a Jupyter Notebook demonstrating **key components** of my Kaggle RNA 3D Folding pipeline, refactored into a simplified, self-contained demo.

## Features

### 1. YAML Conversion
Convert raw RNA sequences into per-target YAML configs for downstream inference.

Output schema (minimal for inference):
id: <sequence_id>
sequence: <ACGU...>
constraints: []

---

### 2. Readable Data Loader
Load and standardize CSV inputs into a validated, tidy DataFrame.

Key operations:
• Ensures required columns (target_id, sequence)
• Cleans invalid characters
• Drops empty/duplicate rows

---

### 3. Two-Model Ensemble
Unified wrapper for two predictors (Boltz-1 and Protenix) with simple ensembling strategies.

Available strategies:
• Mean ensemble
• Rank-average ensemble
