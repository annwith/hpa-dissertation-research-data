# HPA Dissertation Research Data

This repository contains research data, metadata, configuration files, prediction outputs, and provenance information associated with the master's dissertation on weakly supervised subcellular protein localization in individual cells using Human Protein Atlas (HPA) data.

The repository is intended to accompany the dataset deposited in the **Repositório de Dados de Pesquisa da Unicamp (REDU)**. It is not a standalone training codebase. The implementation code used in the dissertation is distributed across separate GitHub repositories listed below.

## Scope of this repository

This repository contains:

* class mappings used by the models and dissertation figures;
* source-data documentation for figures and tables;
* inference notebooks used to generate Kaggle submissions;
* training configuration files;
* model prediction files;
* train/validation/test split manifests;
* metadata needed to trace dissertation figures, tables, and results back to their source experiments.

Raw HPA/Kaggle image files are not redistributed here. When figures depend on raw images, this repository provides sample identifiers so that the original files can be located in the source datasets.

## Related code repositories

The code used in the dissertation is split across three main repositories.

### Baseline

Repository: [annwith/wsss-hpa](https://github.com/annwith/wsss-hpa/tree/main)

This repository contains the code used for the baseline weakly supervised HPA experiments. Files and folders named `baseline` in this research-data repository refer to artifacts associated with this baseline implementation, including training configurations, split files, and submission/inference material.

<!--
Commit used in the dissertation:
<hash do commit>
-->

### Reproduction of the Kaggle second-place solution

Part of the dissertation involved reproducing components of the second-place solution from the HPA Single-Cell Classification Kaggle competition.

Original repository: https://github.com/iseekwonderful/HPA-singlecell-2nd-dual-head-pipeline

The original solution is not claimed as an original contribution of this dissertation. In this work, the reproduction followed the original pipeline closely, including the same augmentation strategy, fold split, image set, model architecture and inference procedure.

This repository includes only artifacts generated or organized during the dissertation work, such as configuration files, split manifests, inference notebooks and result tables associated with the reproduction process.

Artifacts related to this branch are stored under:

- `training-configurations/kaggle-2nd-placed-solution/`
- `train-val-test-split/kaggle-2nd-placed-solution/`
- `inference-configurations/2nd-hpa-public-submission-redu.ipynb`

### Conformal Prediction

Repository: [annwith/hpa-individual-cell-classifier](https://github.com/annwith/hpa-individual-cell-classifier)

This repository contains the code used for conformal prediction experiments. In this research-data repository, artifacts related to conformal prediction are stored under `conformal-prediction`.

<!--
Commit used in the dissertation:
<hash do commit>
-->

### DINO

Repository: [annwith/dino-hpa](https://github.com/annwith/dino-hpa/tree/dinov2-update)

This repository contains the DINO-related experiments used in the dissertation. Files and folders named `dino` in this research-data repository refer to artifacts associated with these experiments, including pretext/downstream training configurations and dataset split files.

<!--
Commit used in the dissertation:
<hash do commit>
-->

## Repository structure

```text
hpa-dissertation-research-data/
├── class-mapping/
├── figures-source-data/
├── inference-configurations/
├── model-predictions/
├── train-val-test-split/
├── training-configurations/
└── README.md
```

## Directory description

### `class-mapping/`

This directory contains the class mapping used in the dissertation experiments.

Current file:

```text
class-mapping/
└── class-mapping.md
```

The mapping defines the relationship between model output indices and the HPA subcellular localization classes. It includes:

* original class names in English;
* Portuguese translations used in the dissertation;
* labels used in paper/dissertation figures;
* abbreviations used in figures and tables.

The model output index corresponds to the class identifier. For example, output index `0` corresponds to `Nucleoplasm`, output index `1` corresponds to `Nuclear membrane`, and so on.

### `figures-source-data/`

This directory documents the data sources used to generate figures and tables in the dissertation.

Current files:

```text
figures-source-data/
└── source-data.md
```

The files describe, for each relevant figure or table:

* the original data source;
* the sample IDs used when figures depend on raw images;
* which model predictions or Kaggle submissions were used for result tables;
* which parts of the dissertation depend on Kaggle, HPA, or the reproduced second-place-solution data.

This directory is primarily a provenance record. It helps trace dissertation figures and tables back to their source data, prediction files, and experiments.

### `inference-configurations/`

This directory contains notebooks used for inference and Kaggle public-test submissions.

Current files:

```text
inference-configurations/
├── 1-hpa-cp-public-submission-redu.ipynb
├── 2nd-hpa-public-submission-redu.ipynb
└── hpa-baseline-public-submission-redu.ipynb
```

These notebooks document the inference procedures used to generate submission files and public Kaggle scores reported in the dissertation.

The notebooks correspond to:

* baseline public-test submission;
* conformal-prediction-related and DINO test submission;
* second-place-solution reproduction/adaptation public-test submission.

Kaggle test results reported in the dissertation were obtained by submitting the corresponding prediction/submission files to Kaggle.

### `model-predictions/`

This directory contains model prediction outputs used in dissertation analyses, figures, or tables.

Current files:

```text
model-predictions/
├── hpa-512-rs269-lr0.1-b16-ls0.1-mixup-ema1-cp-m1_predictions.csv
└── pred-hpa2nd-rs50-lr0.0002-b6-aug2nd-adamw-eid-2nd-pw1-cp-fix-preds-2.csv
```

These files store prediction outputs generated by trained models. They are used to support result tables, selected qualitative examples, and analyses involving model outputs.

The file names preserve the original experiment/model identifiers used during the dissertation work.

### `train-val-test-split/`

This directory contains train/validation/test split manifests or dataset metadata used by each experimental branch.

Current structure:

```text
train-val-test-split/
├── baseline/
│   ├── publichpa.csv
│   └── train.csv
├── conformal-prediction/
│   └── 256_train+ext+rare.csv
├── dino/
│   ├── dino-kaggle.csv
│   └── dino.csv
└── kaggle-2nd-placed-solution/
    └── 256_train+ext+rare.csv
```

The subdirectories follow the experimental organization used throughout the dissertation:

* `baseline/`: split and dataset metadata used in the baseline experiments;
* `conformal-prediction/`: data manifests used in conformal prediction experiments;
* `dino/`: split/data manifests used in DINO/DINOv2 experiments;
* `kaggle-2nd-placed-solution/`: data manifest associated with reproduction of the second-place Kaggle solution.

These files are included to make the experimental splits and sample selection traceable. Raw image files are not included.

### `training-configurations/`

This directory contains training configuration files for the experiments reported in the dissertation.

Current structure:

```text
training-configurations/
├── baseline/
│   ├── base-crop-res.txt
│   ├── base-ema.txt
│   ├── base-mixup-crop-res-ema.txt
│   ├── base-mixup-crop-res.txt
│   ├── base-mixup.txt
│   └── base.txt
├── conformal-prediction/
│   ├── rs50-all-cells-pw0.txt
│   ├── rs50-all-cells-pw1.txt
│   ├── rs50-pw0-cp.txt
│   ├── rs50-pw0.txt
│   ├── rs50-pw1-cp-1-from-pw1.txt
│   ├── rs50-pw1-cp-2-from-pw0.txt
│   ├── rs50-pw1.txt
│   └── sin_256_final.yaml
├── dino/
│   ├── dino-rs50-pretext.txt
│   ├── dino-vit-pretext.txt
│   ├── rs50-down-imagenet.txt
│   └── rs50-down.txt
└── kaggle-2nd-placed-solution/
    ├── sin_256_final.yaml
    ├── sin_exp5_b3_rare.yaml
    ├── sin_exp5_b5_rare.yaml
    ├── sin_exp5_r200d_rarex2.yaml
    ├── sin_exp5_r50d_rarex2.yaml
    └── sin_exp5_rare-se50.yaml
```

These files record the hyperparameters and training settings used in the dissertation experiments, including architecture choices, learning rates, batch sizes, weight decay, augmentation settings, model initialization, and other relevant parameters.

The organization mirrors the main experimental branches:

* `baseline`: baseline weakly supervised HPA models;
* `conformal-prediction`: ResNeSt-50 and conformal prediction experiments;
* `dino`: DINO pretext and downstream experiments;
* `kaggle-2nd-placed-solution`: reproduced configurations from the second-place Kaggle solution.

## Experimental branches

This repository uses four labels to distinguish the origin of artifacts:

| Label                        | Meaning                                          | Related code repository                                |
| ---------------------------- | ------------------------------------------------ | ------------------------------------------------------ |
| `baseline`                   | Baseline experiments                             | `annwith/wsss-hpa`                                     |
| `kaggle-2nd-placed-solution` | Reproduction of the second-place Kaggle solution | `iseekwonderful/HPA-singlecell-2nd-dual-head-pipeline` |
| `conformal-prediction`       | Conformal prediction experiments                 | `annwith/hpa-individual-cell-classifier`               |
| `dino`                       | DINO experiments                                 | `annwith/dino-hpa`                                     |

## Data availability

The raw HPA/Kaggle image data are not redistributed in this repository. They should be obtained from the original sources.

This repository provides derived or auxiliary research artifacts needed to interpret and reproduce the dissertation results, including:

* sample identifiers;
* split manifests;
* prediction files;
* training and inference configurations;
* source-data documentation for figures and tables.

## Reproducibility notes

To reproduce or audit the dissertation results, use this repository together with the corresponding code repositories:

1. Identify the experimental branch: `baseline`, `conformal-prediction`, `kaggle-2nd-placed-solution`, or `dino`.
2. Locate the corresponding training configuration in `training-configurations/`.
3. Locate the corresponding data split or manifest in `train-val-test-split/`.
4. Use the relevant implementation repository listed above.
5. For Kaggle public-test results, inspect the notebooks in `inference-configurations/`.
6. For dissertation tables and qualitative figures, inspect `figures-source-data/` and `model-predictions/`.

## REDU deposit

This repository is intended to accompany the REDU deposit for the dissertation research data.

REDU DOI:

```text
To be added after REDU publication.
```

Suggested REDU dataset title:

```text
Dados derivados e resultados experimentais para classificação fracamente supervisionada da localização subcelular de proteínas em células individuais
```

## Citation

If using this repository, please cite the dissertation and the associated REDU dataset.

```text
To be added after dissertation/REDU publication.
```

## Author

Juliana Midlej do Espírito Santo
Institute of Computing, University of Campinas (Unicamp)

## License

To be defined.

This repository contains metadata, configuration files, prediction outputs, and derived research artifacts. Raw third-party image data are not redistributed.
