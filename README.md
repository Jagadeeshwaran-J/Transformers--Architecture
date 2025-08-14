# 🧠 Transformers Explained: Comprehensive Notes

This repository contains detailed, organized notes extracted from a YouTube video transcript titled **"Transformers Explained."**  
The goal is to provide a simplified and intuitive understanding of the Transformer deep learning architecture, which is fundamental to modern AI advancements like **Large Language Models (LLMs)** such as GPT.

---



## ✨ Key Concepts Covered (So Far)

### 🔡 Understanding Language Models
- The fundamental goal: **predicting the next word**.
- Introduction to models like **BERT** and **GPT** (Large Language Models).

### 🧊 Word Embeddings
- Why text needs **numerical representation**.
- The concept of representing words as **vectors in a multi-dimensional space**.
- Demonstrating semantic relationships through vector arithmetic:  
  _e.g., `King - Man + Woman = Queen`_
- **Static embeddings** (Word2Vec, GloVe) and their limitations.

### 🌐 Contextual Embeddings
- The necessity of **context-aware** word representations.
- How surrounding words **influence a word’s meaning** and its embedding.

### 🏗️ Transformer Architecture Overview
- The two main components: **Encoder** and **Decoder**.
- Their roles in tasks like **next word prediction** and **sentence translation**.
- Distinction between **BERT** (Encoder-only) and **GPT** (Decoder-only).

### 🛠️ Transformer Training Process
- **Self-supervised learning** on massive text datasets.
- The role of **backpropagation** in learning static embeddings and special matrices:  
  `WQ`, `WK`, `WV`.

### 📦 Inside the Encoder (Initial Steps)
- **Tokenization** and special tokens (`[CLS]`, `[SEP]`).
- Combining static word embeddings with **positional embeddings** to capture word order.

### 🎯 The Attention Mechanism — “Attention Is All You Need”
- The core innovation allowing words to “**attend**” to others for contextual understanding.
- The concept of **attention weights/scores**.

### 🧮 Query, Key, and Value (QKV)
- An intuitive analogy (library, professor) to explain **Q**, **K**, and **V**.
- How Q, K, and V vectors are derived from **positional embeddings** using learned matrices:  
  `WQ`, `WK`, `WV`.
- Calculation of **attention scores** using **dot products** and the **Softmax** function.

