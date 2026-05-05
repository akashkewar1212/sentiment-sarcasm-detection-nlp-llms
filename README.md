# Sentiment Analysis and Sarcasm Detection in Product Reviews using NLP and LLMs

## Project Overview

This project focuses on sentiment analysis and sarcasm detection in online product reviews using Natural Language Processing (NLP), machine learning, transformer-based models, and large language models.

Online product reviews are widely used by customers and businesses to understand product quality and user satisfaction. However, sarcasm creates a major challenge because users may express negative opinions using positive words. For example, a review such as:

> “Wow, amazing product. It stopped working in one day.”

may appear positive at first, but the actual meaning is negative.

The aim of this project is to compare different models and understand how well they handle sentiment classification and sarcasm detection.

---

## Objectives

- To prepare and preprocess product review data
- To classify reviews into positive, negative, and neutral sentiment
- To detect whether a review is sarcastic or standard
- To compare traditional machine learning, transformer-based models, and large language models
- To analyse how sarcasm affects sentiment classification

---

## Models Used

The following models were implemented and compared:

| Model | Purpose |
|------|---------|
| SVM | Traditional machine learning baseline |
| Fine-tuned BERT | Transformer-based classification |
| Zero-shot BERT | Classification without task-specific training |
| LLaMA-3 | Prompt-based large language model inference |

---

## Dataset

The dataset was based on Amazon product reviews. The original data was cleaned and reduced to the most relevant columns:

- Review text
- Rating

For sentiment analysis, ratings were converted into labels:

| Rating | Sentiment Label |
|------|----------------|
| 4–5 | Positive |
| 3 | Neutral |
| 1–2 | Negative |

For sarcasm detection, real product reviews were treated as standard reviews, while additional sarcastic examples were synthetically generated for classification.

---

## Project Workflow

The project follows this general workflow:

```text
Dataset Collection
        ↓
Data Cleaning and Preprocessing
        ↓
Text Representation
        ↓
Model Training / Inference
        ↓
Prediction
        ↓
Evaluation and Analysis

**Results Summary**
Model	                     Sentiment Accuracy	          Sarcasm Accuracy
SVM	                           89%	                        99%
Fine-tuned BERT	               92%	                        99%
Zero-shot BERT	               50%	                        61%
LLaMA-3	                       49%	                        70%

The fine-tuned BERT model achieved the strongest overall performance. SVM also performed well on structured data but relied heavily on word patterns. Zero-shot BERT and LLaMA-3 showed better generalisation on unseen examples but were less consistent overall

**## Key Findings**

- Sarcasm can significantly affect sentiment classification.
- High accuracy does not always mean better understanding.
- SVM relies strongly on lexical patterns.
- Fine-tuned BERT performs well because it captures context better.
- LLaMA-3 shows promise for understanding implicit meaning but requires better prompting or fine-tuning.
- Real-world sarcastic reviews would improve future model reliability

**Limitations**
- The dataset size was relatively small.
- Some sarcastic examples were generated rather than collected from real users.
- Sentiment analysis and sarcasm detection were treated as separate tasks.
- LLaMA-3 was used through prompting and was not fine-tuned.

**Future Work**
Future improvements could include:

- Collecting real-world sarcastic product reviews
- Combining sarcasm detection and sentiment classification into one task
- Adding emotion detection
- Fine-tuning large language models
- Building a deployable web application for real-time review analysis

## Author

Akash Kewar  
MSc Data Science  
Robert Gordon University  

LinkedIn: https://www.linkedin.com/in/akash-kewar-5a0265199/

## Acknowledgement

I would like to thank my supervisor, Dr. Kyle Martin, for his guidance and support throughout this project.
