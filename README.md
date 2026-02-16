# rnn-llama-rag-labs
NLP, Deep Learning and LLM Labs: RNN sentiment analysis, LLaMA comparison, and RAG system
# RNN, LLaMA, and RAG Labs

This repository contains three laboratory exercises demonstrating the progression from
traditional deep learning models to large language models (LLMs) and Retrieval-Augmented
Generation (RAG).

---

## Lab Exercise 1 — RNN for Text Classification

### Goal
Train a Recurrent Neural Network (RNN) to classify movie reviews as **Positive** or **Negative**.

### Dataset
- IMDB Movie Reviews
- 50,000 samples
- Binary sentiment labels

### Steps
1. Load and clean dataset
2. Train-test split (80% / 20%)
3. Text preprocessing:
   - Tokenization
   - Padding sequences
4. Build RNN model:
   - Embedding layer
   - LSTM layer
   - Dense output layer
5. Train the model
6. Evaluate accuracy and plot loss/accuracy

### Output
- Training and validation accuracy
- Final test accuracy
  
![Lab 1 Accuracy](https://raw.githubusercontent.com/AliHassanRaza9/rnn-llama-rag-labs/main/images/lab1_accuracy.png)


---

## Lab Exercise 2 — LLaMA Sentiment Analysis with Ollama

### Goal
Run a pre-trained LLaMA model locally using **Ollama** and compare its performance with the RNN.

### Tools
- Ollama
- LLaMA / Gemma model
- Python + Jupyter Notebook

### Steps
1. Install Ollama
2. Run LLaMA locally
3. Send movie reviews as prompts
4. Record predictions
5. Compare predictions with ground truth
6. Calculate accuracy

### Comparison

| Model | Accuracy | Strengths | Weaknesses |
|------|--------|----------|-----------|
| RNN | ~88% | Simple, low cost | Lower contextual understanding |
| LLaMA | ~94% | High accuracy, strong language understanding | Higher compute cost |

---

## Lab Exercise 3 — Retrieval-Augmented Generation (RAG)

### Goal
Build a Question–Answering system using custom documents + LLaMA.

### Steps
1. Prepare documents and split into chunks
2. Generate embeddings using SentenceTransformers
3. Perform similarity search
4. Build RAG prompt
5. Compare:
   - LLaMA alone
   - LLaMA + RAG

### Results
RAG significantly reduces hallucinations and improves answer accuracy by grounding responses
in provided documents. 
### Lab 3 Results — RAG vs No-RAG

| Method | Correct (out of 10) | Notes |
|------|-------------------|------|
| LLaMA alone | 7 | May hallucinate |
| LLaMA + RAG | 10 | More accurate |

RAG improved accuracy from 70% to 100% by grounding answers in retrieved document context.


---

## How to Run
```bash
pip install -r requirements.txt
