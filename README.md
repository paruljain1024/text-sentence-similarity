# text-sentence-similarity
text sentence similarity
# TOPSIS-Based Evaluation of Pretrained Models for Sentence Similarity  

## Overview  
This project applies **TOPSIS** to compare and rank **pretrained models** for **text sentence similarity**.  

## Objective  
Identify the **best-performing pretrained model** for sentence similarity based on multiple criteria, including:  
- **Accuracy (Cosine Similarity)**  
- **Inference Time**  
- **Model Size**  

## Dataset & Evaluation  
We tested three popular **pretrained models** on a set of **sentence pairs**:  
- **BERT (bert-base-uncased)**  
- **RoBERTa (sentence-transformers/all-roberta-large-v1)**  
- **SBERT (sentence-transformers/all-MiniLM-L6-v2)**  

Each model was evaluated on:  
✔ **Cosine Similarity (Higher is better)**  
✔ **Inference Time (Lower is better)**  
✔ **Model Size (Lower is better)**  

## ⚙️ Implementation Steps  
1️⃣ **Load Pretrained Models** using `sentence-transformers`  
2️⃣ **Compute Sentence Similarity Scores**  
3️⃣ **Measure Inference Time & Model Size**  
4️⃣ **Normalize the Data**  
5️⃣ **Apply TOPSIS Algorithm**  
6️⃣ **Rank Models Based on Performance**  

## Results & Rankings  

| Model | Cosine Similarity | Inference Time (s) | Model Size (MB) | TOPSIS Score | Rank |
|-------|------------------|------------------|--------------|-------------|------|
| **RoBERTa** | 0.4911 | 0.4559 | 1355.59 | 0.6706 | 1st |
| **BERT** | 0.7434 | 0.1320 | 417.64 | 0.4538 | 2nd |
| **SBERT** | 0.3876 | 0.1483 | 86.64 | 0.0286 | 3rd |

**Best Model** → **RoBERTa (sentence-transformers/all-roberta-large-v1)**  

### **Visualization**  
TOPSIS ranking of models based on multiple criteria:  

![TOPSIS Ranking](Topsis_Ranking.png)  

##  Setup & Usage  

###  **Install Dependencies**  
```bash
pip install transformers sentence-transformers numpy pandas scikit-learn matplotlib
