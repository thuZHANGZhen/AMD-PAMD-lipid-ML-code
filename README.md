# AMD/PAMD ionizable lipid machine-learning code

This repository contains the Jupyter notebooks used for machine-learning analysis of the AMD/PAMD combinatorial ionizable-lipid library. The code accompanies the revised manuscript and is provided to support methodological review and reproducibility.

## Notebooks

- `baseline_models_v1.ipynb`: baseline preprocessing and model comparison.
- `unified_preprocessing_v1.ipynb`: model comparison using a unified preprocessing workflow.
- `scaffold_group_validation_head_v1.ipynb`: head-group/scaffold-aware validation.
- `scaffold_group_validation_tail_v1.ipynb`: tail-group/scaffold-aware validation.

## Expected input layout

The notebooks expect input files under `data/` by default:

```text
data/
├── Dataset.xlsx
└── Sequential structure of the heat map/
    ├── head/
    └── tail/
```

The dataset and molecular-structure files are not included in this code-only repository. Set the `AMD_PAMD_DATA_DIR` environment variable if the inputs are stored elsewhere. Generated models and CSV files are written to `outputs/`; set `AMD_PAMD_OUTPUT_DIR` to use another output directory.

## Installation

Python 3.10 or later is recommended.

```bash
python -m venv .venv
python -m pip install -r requirements.txt
jupyter lab
```

Package versions are intentionally specified as minimum compatible versions because the notebooks were developed across multiple analysis iterations. For exact archival reproduction, record the resolved environment with `python -m pip freeze` after installation.

## Notes

- Saved notebook outputs and execution counts were removed from the public copy.
- Local absolute paths were replaced by portable, repository-relative paths.
- Random seeds used by the analysis remain in the notebooks.

