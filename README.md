# StudyMate

## Table of Contents

1. [Introduction](#introduction)
2. [Datasets](#datasets)
3. [Models](#models)
4. [Results](#results)

## Introduction

Provide a brief introduction to the project. Explain the purpose, objectives, and any background information necessary to understand the context of the project.

## Datasets

### Dataset 1: BanglaRQA

- Source: [BanglaRQA on Hugging Face](https://huggingface.co/datasets/sartajekram/BanglaRQA)

### Dataset 2: SQuAD_bn

- Source: [SQuAD_bn on Hugging Face](https://huggingface.co/datasets/csebuetnlp/squad_bn)

### Filtered Dataset of BanglaRQA: BanglaRQA_to_SquadBn_fact_confirm

- Description: Filtered dataset of BanglaRQA involving factoid and confirmation type questions in SQuAD_bn format
- Source: [BanglaRQA_to_SquadBn_fact_confirm on Hugging Face](https://huggingface.co/datasets/shakun42/BanglaRQA_to_SquadBn_fact_confirm)

## Models

4 BERT based models were used: XLM-RoBERTa, mBert, BanglaBERT and IndicBERT were used on the 2 the datasets to produce a total of 8 models.

### SQuAD_bn Trained Models

#### Model 1: xlm-roberta-base-finetuned-squadBN

- Link: [xlm-roberta-base-finetuned-squadBN](https://huggingface.co/AsifAbrar6/xlm-roberta-base-finetuned-squadBN)

#### Model 2: bert-base-multilingual-cased-finetuned-squadBN

- Link: [bert-base-multilingual-cased-finetuned-squadBN](https://huggingface.co/AsifAbrar6/bert-base-multilingual-cased-finetuned-squadBN)

#### Model 3: bangla-bert-base-finetuned-squadbn

- Link: [bangla-bert-base-finetuned-squadbn](https://huggingface.co/shakun42/bangla-bert-base-finetuned-squadbn)

#### Model 4: indic-bert-finetuned-squadbn

- Link: [indic-bert-finetuned-squadbn](https://huggingface.co/shakun42/indic-bert-finetuned-squadbn)

### BRQA Trained Models

#### Model 1: xlm-roberta-base-finetuned-RQA-confirmation

- Link: [xlm-roberta-base-finetuned-RQA-confirmation](https://huggingface.co/AsifAbrar6/xlm-roberta-base-finetuned-RQA-confirmation)

#### Model 2: bert-base-multilingual-cased-finetuned-RQA

- Link: [bert-base-multilingual-cased-finetuned-RQA](https://huggingface.co/AsifAbrar6/bert-base-multilingual-cased-finetuned-RQA)

#### Model 3: bangla-bert-base-finetuned-brqa-confirmation

- Link: [bangla-bert-base-finetuned-brqa-confirmation](https://huggingface.co/shakun42/bangla-bert-base-finetuned-brqa-confirmation)

#### Model 4: indic-bert-finetuned-brqa-confirmation

- Link: [indic-bert-finetuned-brqa-confirmation](https://huggingface.co/shakun42/indic-bert-finetuned-brqa-confirmation)

## Results

### Model 1

- Accuracy: [Provide accuracy]
- Other Metrics: [Provide other relevant metrics]

### Model 2

- Accuracy: [Provide accuracy]
- Other Metrics: [Provide other relevant metrics]

### Additional Results

- If you have more results, follow the same format as above for each additional model.

## Evaluations

| Model                | exact              | f1                 | total | HasAns_exact       | HasAns_f1          | HasAns_total | NoAns_exact         | NoAns_f1            | NoAns_total | best_exact         | best_exact_thresh | best_f1            | best_f1_thresh |
| -------------------- | ------------------ | ------------------ | ----- | ------------------ | ------------------ | ------------ | ------------------- | ------------------- | ----------- | ------------------ | ----------------- | ------------------ | -------------- |
| BanglaBERT_Base_BRQA | 18.95093062605753  | 29.891786130011873 | 1182  | 25.806451612903224 | 40.705174200085295 | 868          | 0.0                 | 0.0                 | 314         | 26.73434856175973  | 0.0               | 31.799368113736023 | 0.0            |
| BanglaBERT_SquadBN   | 9.25               | 16.132710539947382 | 1200  | 17.44              | 30.654804236698972 | 625          | 0.34782608695652173 | 0.34782608695652173 | 575         | 47.916666666666664 | 0.0               | 47.97222222222222  | 0.0            |
| IndicBERT-BanglaRQA  | 10.829103214890017 | 24.94270420474983  | 1182  | 13.940092165898617 | 33.159304573749196 | 868          | 2.229299363057325   | 2.229299363057325   | 314         | 26.56514382402707  | 0.0               | 27.684840734822945 | 0.0            |
| IndicBERT-SquadBN    | 6.75               | 14.464655088919802 | 1200  | 12.8               | 27.61213777072602  | 625          | 0.17391304347826086 | 0.17391304347826086 | 575         | 47.916666666666664 | 0.0               | 47.916666666666664 | 0.0            |
| XLM-Base-RQA         | 47.88494077834179  | 60.038975495562674 | 1182  | 64.97695852534562  | 81.5277293038653   | 868          | 0.6369426751592356  | 0.6369426751592356  | 314         | 47.71573604060914  | 0.0               | 59.86977075782999  | 0.0            |
| XLM-Base-SquadBN     | 23.583333333333332 | 31.319512540836108 | 1200  | 45.28              | 60.133464078405325 | 625          | 0.0                 | 0.0                 | 575         | 48.0               | 0.0               | 48.0               | 0.0            |
| mBert-Base-RQA       | 46.36209813874788  | 58.77937274709887  | 1182  | 63.133640552995395 | 80.04287855653325  | 868          | 0.0                 | 0.0                 | 314         | 46.36209813874788  | 0.0               | 58.77937274709885  | 0.0            |
| mBert-Base-SquadBN   | 25.0               | 32.49190584742056  | 1200  | 46.88              | 61.26445922704749  | 625          | 1.2173913043478262  | 1.2173913043478262  | 575         | 48.0               | 0.0               | 48.0               | 0.0            |

```

```
