# MSAI6320 Unit 4 Lab: Logistic Regression and Text Classification

Airline customer-message triage for MSAI6320 (Natural Language Processing, Birzeit University). The notebook builds logistic regression from scratch, extends it to three classes with softmax, evaluates it, and ends with a team competition to classify tweets as negative, neutral or positive.

## Contents

| Path | What it is |
|---|---|
| `MSAI6320_LogReg_and_TextClassification.ipynb` | The lab notebook with Tasks 3 to 9 completed |
| `Data/` | `train.csv` (10,084 messages), `dev.csv` (2,161), `test_public.csv` (2,161, no labels), `sentiment_lexicon.csv` |
| `submissions/Rayyan_And_Ameer_s_Team.csv` | Predictions for the 2,161 test messages (columns `id`, `label`) |
| `requirements.txt` | Python packages used |

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook MSAI6320_LogReg_and_TextClassification.ipynb
```

The notebook reads its data from `Data/`. Use Kernel, then Restart & Run All to reproduce every result.

## Task 9 model

Word 1 to 2 gram and character 2 to 5 gram TF-IDF features (with links and `@handles` collapsed to single tokens), fed to logistic regression with `C=3` and balanced class weights.

| Model | Dev macro-F1 |
|---|---|
| Starter model | 0.704 |
| Instructor's baseline | 0.743 |
| This model (trained on train only) | 0.751 |

The submission file comes from the same model refit on train plus dev. The dev score above is from the train-only fit. Differences of about 0.01 are within noise at this dataset size.

## Data license

`Data/` comes from Twitter US Airline Sentiment (Crowdflower / Figure Eight), licensed CC BY-NC-SA 4.0. See `Data/README.md` for the changes made to it.
