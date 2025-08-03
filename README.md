# Generalisation in Text Mining

This repository contains the code, data organization, and scripts used for my master's thesis on generalisation in Named Entity Recognition (NER).

---

## Table of Contents

- [Overview](#overview)
- [Directory Structure](#directory-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Scripts](#scripts)
- [Augmentation Code](#augmentation-code)
- [Results](#results)
- [References](#references)
- [License](#license)

---

## Overview

This project investigates the generalisation ability of NER models, focusing on performance across different domains and with various augmentation strategies. The experiments include fine-tuning BERT-based models, evaluating on OntoNotes and custom challenge sets, and analyzing the effects of guided adversarial augmentation.

---

## Directory Structure

```text
.
├── data/                   # Challenge sets, and datasets
│   ├── Africa_ner_challenge.csv
│   ├── Asia_ner_challenge.csv
│   ├── ...                 # Other regional challenge sets
│   ├── conll-2012/         # OntoNotes 5.0 data (full structure not shown)
│   └── onto_newswire_en/   # segregated dataset using only newswire sources
├── Guided-Adversarial-Augmentation-main/
│   ├── code/BERT/          # Data augmentation and NER scripts
│   └── data/conll2003/     # Augmented data variants
├── Literature/             # Research papers and references
├── output/bert-base-cased/ # Model outputs/checkpoints
├── scripts/                # Jupyter notebooks for analysis and evaluation
├── LICENSE
└── README.md
```

_Note: **`conll-2012/`** follows the official OntoNotes directory structure (see _[_OntoNotes documentation_](https://catalog.ldc.upenn.edu/docs/LDC2013T19/OntoNotes-Release-5.0.pdf)_)._

---

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Matt081297/Nikhil_Mathews_Generalisation_Text_Mining.git
   cd Nikhil_Mathews_Generalisation_Text_Mining
   ```

2. **Set up a virtual environment (recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   ```

3. **Install required packages:**

   ```bash
   pip install -r requirements.txt
   ```

   _Note: Some scripts and notebooks may require additional libraries for data processing and model training (see individual notebook/script headers for details)._

---

## Usage

- **Main experiments** can be launched by running relevant Jupyter notebooks in the `scripts/` folder.

---

## Data

- **Challenge sets:**\
  Contained in `data/` as CSV files, covering different world regions and linguistic contexts.

- **Main dataset:**

  - `data/conll-2012/` contains the OntoNotes 5.0 corpus, structured by the official release.
  - `data/onto_newswire_en/` and other subfolders provide additional or processed datasets.
  - A lot of saved splits were not saved as files were individually greater than 100Mb and not allowed on github

- **Stanford Challenge datasets:**\
  Located in `Guided-Adversarial-Augmentation-main/data/conll2003/`, used for evaluating generalisation.

_Some datasets are large and may require external download or extraction. See dataset documentation for access and licensing._

---

## Scripts

- Jupyter notebooks in `scripts/` cover:

  - Data analysis and exploration
  - Model training and fine-tuning
  - Evaluation and error analysis
  - Seed variability and experiment reproducibility

- Notebooks and scripts are named by purpose. Please check each file header for specific usage.

---

## Results

- Model checkpoints and main evaluation results are saved in `output/bert-base-cased/` and in output files specified by scripts.
- Main results, saved models, etc were not uploaded as files were individually greater than 100Mb and not allowed on github
- Summary tables, figures, and error analyses are presented in the main thesis document and supplementary Jupyter notebooks.

---

## References

Key literature and resources can be found in the `Literature/` folder, including:

- Research papers on NER generalisation and data augmentation
- Core NLP and BERT literature

---

## License

This project is licensed under the terms of the [MIT License](LICENSE).

---

_For questions, clarifications, or collaboration, please contact the repository owner via GitHub._
