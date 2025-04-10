# Medical Question Summarization with Synthetic Data Augmentation

[![GitHub license](https://img.shields.io/github/license/your-username/your-repo-name)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8-blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=flat&logo=jupyter&logoColor=white)](https://jupyter.org/)

## Project Overview
This project addresses the challenge of improving healthcare question summarization using synthetic data augmentation. By leveraging **Round-Trip Translation (RTT)** and advanced selection techniques (**FQD**, **PRQD**, and **QSV**), we generate diverse question paraphrases to enhance summarization model performance in low-resource settings.

### Key Objectives:
1. **Dataset Augmentation**: Use RTT to create synthetic variations of medical questions.
2. **Question Selection**: Filter augmented questions using:
   - Frechét Question Distance (FQD)
   - Precision-Recall Question Distance (PRQD)
   - Question Semantic Volume (QSV)
3. **Summarization**: Train and evaluate models like BART/T5 on the augmented dataset.
4. **Evaluation**: Compare results using ROUGE/BLEU metrics.

---

## Dataset
- **MEQSUM Dataset**: Used for medical question summarization tasks.
- Contains pairs of:  
  - Original questions (symptoms, treatments, diagnosis, medications)
  - Expert-annotated summaries

---

## Methodology
### 1. Round-Trip Translation (RTT)
Translate questions to 5 languages (Spanish, German, Italian, Chinese, French) and back to English to generate paraphrased questions.

### 2. Question Selection
- **FQD**: Measures semantic distribution similarity between original and augmented questions.
- **PRQD**: Balances precision and recall of semantic overlap.
- **QSV**: Selects questions with maximum semantic diversity using PCA and convex hulls.

### 3. Summarization Models
Tested with pretrained models like:
- **BART**
- **T5**
- **ProphetNet**

---

## Repository Structure
- `notebooks/`: Contains Jupyter notebooks with full implementation.
- `docs/`: Final project report and visualization results and project description.

---
