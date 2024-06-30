# StudyMate

## Table of Contents

1. [Introduction](#introduction)
2. [Datasets](#datasets)
3. [Models](#models)
4. [Results](#results)

## Introduction

StudyMate is a multilingual extractive question-answering application tailored for Bangla-speaking students. It compares and deploys models trained on Bangla datasets to deliver precise answers swiftly, enhancing academic learning and performance.

## Datasets

### BanglaRQA

- Source: [BanglaRQA on Hugging Face](https://huggingface.co/datasets/sartajekram/BanglaRQA)

### SQuAD_bn

- Source: [SQuAD_bn on Hugging Face](https://huggingface.co/datasets/csebuetnlp/squad_bn)

### Filtered Dataset of BanglaRQA: BanglaRQA_to_SquadBn_fact_confirm

Filtered dataset of BanglaRQA involving factoid and confirmation type questions converted to SQuAD_bn dataset format

- Source: [BanglaRQA_to_SquadBn_fact_confirm on Hugging Face](https://huggingface.co/datasets/shakun42/BanglaRQA_to_SquadBn_fact_confirm)

## Models

4 BERT based models [XLM-RoBERTa](https://huggingface.co/FacebookAI/xlm-roberta-base), [mBert](https://huggingface.co/google-bert/bert-base-multilingual-cased), [BanglaBERT](https://huggingface.co/sagorsarker/bangla-bert-base) and [IndicBERT](https://huggingface.co/ai4bharat/indic-bert) were used on the 2 the datasets to produce a total of 8 models as follows:

### SQuAD_bn Trained Models

#### XLM-RoBERTa

- Link: [xlm-roberta-base-finetuned-squadBN](https://huggingface.co/AsifAbrar6/xlm-roberta-base-finetuned-squadBN)

#### mBERT

- Link: [bert-base-multilingual-cased-finetuned-squadBN](https://huggingface.co/AsifAbrar6/bert-base-multilingual-cased-finetuned-squadBN)

#### BanglaBERT

- Link: [bangla-bert-base-finetuned-squadbn](https://huggingface.co/shakun42/bangla-bert-base-finetuned-squadbn)

#### IndicBERT

- Link: [indic-bert-finetuned-squadbn](https://huggingface.co/shakun42/indic-bert-finetuned-squadbn)

### BanglaRQA Trained Models

#### XLM-RoBERTa

- Link: [xlm-roberta-base-finetuned-RQA-confirmation](https://huggingface.co/AsifAbrar6/xlm-roberta-base-finetuned-RQA-confirmation)

#### mBERT

- Link: [bert-base-multilingual-cased-finetuned-RQA](https://huggingface.co/AsifAbrar6/bert-base-multilingual-cased-finetuned-RQA)

#### BanglaBERT

- Link: [bangla-bert-base-finetuned-brqa-confirmation](https://huggingface.co/shakun42/bangla-bert-base-finetuned-brqa-confirmation)

#### IndicBERT

- Link: [indic-bert-finetuned-brqa-confirmation](https://huggingface.co/shakun42/indic-bert-finetuned-brqa-confirmation)

## Code

The code for training the models is provided in the repository

## Running the application

To run the application, just run the notebook [here](./Project_UI_Gradio.ipynb)

## Results

### F1 Score and Exact Match on SQuAD_bn dataset

<table>
  <thead>
    <tr>
      <th>Models</th>
      <th>HasAns Total</th>
      <th>HasAns Exact</th>
      <th>HasAns F1</th>
      <th>NoAns Total</th>
      <th>NoAns Exact</th>
      <th>NoAns F1</th>
      <th>Exact</th>
      <th>F1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bangla BERT</td>
      <td>625</td>
      <td>15.52</td>
      <td>27.29</td>
      <td>575</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>8.08</td>
      <td>14.22</td>
    </tr>
    <tr>
      <td>Indic BERT</td>
      <td>625</td>
      <td>12.80</td>
      <td>27.61</td>
      <td>575</td>
      <td>0.17</td>
      <td>0.17</td>
      <td>6.75</td>
      <td>14.46</td>
    </tr>
    <tr>
      <td>XLM Roberta</td>
      <td>625</td>
      <td>45.28</td>
      <td>60.13</td>
      <td>575</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>23.58</td>
      <td>31.31</td>
    </tr>
    <tr>
      <td>mBert</td>
      <td>625</td>
      <td><strong>46.88</strong></td>
      <td><strong>61.26</strong></td>
      <td>575</td>
      <td><strong>1.21</strong></td>
      <td><strong>1.21</strong></td>
      <td><strong>25.00</strong></td>
      <td><strong>32.49</strong></td>
    </tr>
  </tbody>
</table>
<p><strong>Table:</strong> Quantitative Evaluation of Various Models on SquadBN Dataset</p>

### F1 Score and Exact Match on BanglaRQA dataset

<table>
  <thead>
    <tr>
      <th>Models</th>
      <th>HasAns Total</th>
      <th>HasAns Exact</th>
      <th>HasAns F1</th>
      <th>NoAns Total</th>
      <th>NoAns Exact</th>
      <th>NoAns F1</th>
      <th>Exact</th>
      <th>F1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bangla BERT</td>
      <td>868</td>
      <td>26.84</td>
      <td>41.91</td>
      <td>314</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>19.71</td>
      <td>30.77</td>
    </tr>
    <tr>
      <td>Indic BERT</td>
      <td>868</td>
      <td>13.94</td>
      <td>33.16</td>
      <td>314</td>
      <td><strong>2.23</strong></td>
      <td><strong>2.23</strong></td>
      <td>10.83</td>
      <td>24.94</td>
    </tr>
    <tr>
      <td>XLM Roberta</td>
      <td>868</td>
      <td><strong>64.98</strong></td>
      <td><strong>81.53</strong></td>
      <td>314</td>
      <td>0.64</td>
      <td>0.64</td>
      <td><strong>47.89</strong></td>
      <td><strong>60.04</strong></td>
    </tr>
    <tr>
      <td>mBert</td>
      <td>868</td>
      <td>63.13</td>
      <td>80.04</td>
      <td>314</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>46.36</td>
      <td>58.78</td>
    </tr>
  </tbody>
</table>
<p><strong>Table:</strong> Quantitative Evaluation of Various Models on BanglaRQA Dataset</p>

### Training and Validation loss

## Loss with SQuAD_bn dataset

<table>
  <thead>
    <tr>
      <th>Models</th>
      <th>Training Loss</th>
      <th>Evaluation Loss</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bangla BERT</td>
      <td>1.82</td>
      <td>2.26</td>
    </tr>
    <tr>
      <td>Indic BERT</td>
      <td>2.79</td>
      <td>2.74</td>
    </tr>
    <tr>
      <td>XLM Roberta</td>
      <td>1.17</td>
      <td>1.39</td>
    </tr>
    <tr>
      <td>mBert</td>
      <td>0.88</td>
      <td>1.46</td>
    </tr>
  </tbody>
</table>
<p><strong>Table:</strong> Training and Evaluation Loss of Various Models on SquadBN Dataset</p>

## Loss with BanglaRQA dataset

<table>
  <thead>
    <tr>
      <th>Models</th>
      <th>Training Loss</th>
      <th>Evaluation Loss</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Bangla BERT</td>
      <td>1.07</td>
      <td>1.41</td>
    </tr>
    <tr>
      <td>Indic BERT</td>
      <td>1.40</td>
      <td>1.44</td>
    </tr>
    <tr>
      <td>XLM Roberta</td>
      <td>0.59</td>
      <td>0.73</td>
    </tr>
    <tr>
      <td>mBert</td>
      <td>0.34</td>
      <td>0.64</td>
    </tr>
  </tbody>
</table>
<p><strong>Table:</strong> Training and Evaluation Loss of Various Models on BanglaRQA Dataset</p>

### Images

The loss curves are provided in the folder [here](./Images/)

<!--
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

``` -->
