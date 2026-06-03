# Figure and table source data

This file documents the data sources used to generate the figures and tables in the dissertation. Raw third-party data from Kaggle, the Human Protein Atlas, and the second-place solution are not redistributed in this deposit. When figures depend on third-party raw data, only the original sample identifiers, source filenames, and derived data used in the dissertation are provided.

## Chapter 2

### Figure 2.16

* Source: Kaggle HPA competition data
* Sample ID: `d0c1b088-bbca-11e8-b2bc-ac1f6b6435d0`
* Raw image redistributed in this deposit: No
* Notes: The figure was generated from the original Kaggle image corresponding to the sample ID above.

## Chapter 3

### Figure 3.1

* Source: Kaggle HPA competition data
* Sample ID: `5b99d3e8-bb99-11e8-b2b9-ac1f6b6435d0`
* Raw image redistributed in this deposit: No
* Notes: The figure was generated from the original Kaggle image corresponding to the sample ID above.

### Figure 3.4

* Source: Kaggle HPA competition data `train.csv`
* Raw `train.csv` redistributed in this deposit: No
* Sample identifiers used in the experiments are provided in `train-val-test-split/baseline/`: 
  * `kaggle-samples-ids.csv` 

### Figure 3.5

* Source: Kaggle HPA competition data `train.csv`
* Raw `train.csv` redistributed in this deposit: No
* Sample identifiers used in the experiments are provided in `train-val-test-split/baseline/`: 
  * `kaggle-samples-ids.csv` 

### Figure 3.6

* Source: Kaggle HPA competition data `train.csv`
* Raw `train.csv` redistributed in this deposit: No
* Sample identifiers used in the experiments are provided in `train-val-test-split/baseline/`: 
  * `kaggle-samples-ids.csv` 

### Figure 3.8

* Source: Kaggle HPA competition data `train.csv` and corresponding image files
* Raw images redistributed in this deposit: No
* Sample identifiers used in this figure are provided:

| Sample ID                              |
| -------------------------------------- |
| `51ef7530-bba5-11e8-b2ba-ac1f6b6435d0` |
| `39c9a9ee-bb9b-11e8-b2b9-ac1f6b6435d0` |
| `982c921a-bbb1-11e8-b2ba-ac1f6b6435d0` |
| `d0c1b088-bbca-11e8-b2bc-ac1f6b6435d0` |
| `0189cff8-bbc0-11e8-b2bb-ac1f6b6435d0` |
| `e2589c84-bbb2-11e8-b2ba-ac1f6b6435d0` |
| `f030c696-bb9a-11e8-b2b9-ac1f6b6435d0` |
| `5f2b97e6-bbc4-11e8-b2bc-ac1f6b6435d0` |
| `d92537b8-bbca-11e8-b2bc-ac1f6b6435d0` |
| `2d491298-bbca-11e8-b2bc-ac1f6b6435d0` |
| `bf433be8-bbc9-11e8-b2bc-ac1f6b6435d0` |
| `b6a469d8-bbad-11e8-b2ba-ac1f6b6435d0` |
| `ca883cf4-bb99-11e8-b2b9-ac1f6b6435d0` |
| `f72cd504-bba7-11e8-b2ba-ac1f6b6435d0` |
| `b64bd070-bb99-11e8-b2b9-ac1f6b6435d0` |
| `6a21830a-bba5-11e8-b2ba-ac1f6b6435d0` |
| `f9fced36-bbb2-11e8-b2ba-ac1f6b6435d0` |
| `1900d278-bbc3-11e8-b2bc-ac1f6b6435d0` |
| `86900d2a-bba2-11e8-b2b9-ac1f6b6435d0` |

## Chapter 4

### Figure 4.2

* Sources:
  * Kaggle HPA competition data `train.csv`
  * HPA `publichpa.csv`
* Raw source files redistributed in this deposit: No
* Sample identifiers used in the experiments are provided in `train-val-test-split/baseline/`: 
  * `kaggle-samples-ids.csv` 
  * `hpa-samples-ids.csv`

### Figure 4.4

* Sources:
  * Kaggle HPA competition data `train.csv`
  * Kaggle second-place solution data `256_train+ext+rare.csv`
* Raw source files redistributed in this deposit: No
* Sample identifiers used in the experiments are provided in `train-val-test-split/kaggle-2nd-placed-solution/` and `train-val-test-split/baseline/`: 
  * `kaggle-samples-ids.csv` 
  * `kaggle-2nd-samples-ids.csv`

### Figure 4.5

* Source: kaggle second-place solution data (they also used Kaggle HPA data)
* Sample ID: `5fb643ee-bb99-11e8-b2b9-ac1f6b6435d0`
* Raw image/data redistributed in this deposit: No
* Notes: The figure was generated from the sample identified above.

<!-- ### Figure 4.7

* Source type: model prediction output
* Model: To be confirmed
* Predictions file: To be confirmed
* Deposited source data: ``
* Notes: The model and prediction file used to generate this figure should be identified before final submission to REDU.

### Figure 4.8

* Source type: model prediction output
* Model: To be confirmed
* Predictions file: To be confirmed
* Deposited source data: ``
* Notes: The model and prediction file used to generate this figure should be identified before final submission to REDU. -->

## Chapter 5

### Table 5.1

* Source type: Kaggle public test submission results
* Platform: Kaggle
<!-- * Models: See `metrics/kaggle_public_scores.csv` -->
* Submission notebook: See `inference-configurations/hpa-baseline-public-submission-redu.ipynb`
* Notes: The reported test results were obtained by submitting a notebook to Kaggle and recording the public leaderboard scores.

### Table 5.3

* Source type: model prediction output
* Predictions file: `predictions/pred-hpa-512-rs269-lr0.1-b16-ls0.1-mixup-ema1-cp-m1.csv`
* Notes: This table was generated from the prediction file listed above. The corresponding model configuration should be provided in the `configs/` directory.

### Figures 5.1 and 5.2

* Source type: model prediction output and selected sample visualization
* Sample names/IDs: specified in the dissertation figure captions.
* Model: specified in the dissertation figure captions.

### Table 5.7

* Source type: model prediction output
* Deposited predictions file: `predictions/pred-hpa2nd-rs50-lr0.0002-b6-aug2nd-adamw-eid-2nd-pw1-cp-fix-preds-2.csv`
