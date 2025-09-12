# 🤖 Transformer Concepts Cheat Sheet

A concise reference guide to core concepts behind the Transformer architecture, including token handling, attention mechanisms, and model internals. Designed for students, researchers, and practitioners working with models like BERT, GPT, T5, and more.

---

## 🔹 Tokenization & Input Representations

- **Token**  
  A single unit of text (word, subword, or character) that the model processes.

- **Tokenization**  
  Splitting raw text into tokens suitable for model input.  
  E.g., `"Transformers are cool"` → `["Transform", "##ers", "are", "cool"]`.

- **Static Vectors (Word Embeddings)**  
  Fixed vector representations of words regardless of context (e.g., Word2Vec, GloVe).

- **Contextual Vectors (Contextual Embeddings)**  
  Word representations that depend on surrounding context.  
  *E.g., “bank” in “river bank” vs. “bank account” has different vectors.*

- **Positional Encoding**  
  Injects information about token positions since Transformers lack inherent sequence order.

---

## 🔹 Attention Mechanism

- **Self-Attention**  
  Each token attends to every other token to compute a context-aware representation.

- **Multi-Head Attention**  
  Runs multiple attention operations in parallel to capture different types of token relationships.

- **Query / Key / Value (QKV)**  
  Projections of input embeddings used to compute attention:
  - **Query (Q)**: What you're looking for
  - **Key (K)**: What you have
  - **Value (V)**: What you retrieve

- **Attention Score**  
  A weight representing how much attention one token gives to another (computed via Q and K).

- **Softmax**  
  Converts raw attention scores into normalized probabilities across tokens.

- **Masking**  
  Prevents the model from attending to certain positions (e.g., padding tokens or future tokens during generation).

---

## 🔹 Transformer Architecture

- **Encoder / Decoder**  
  - **Encoder**: Processes input and encodes contextual representations (used in BERT).
  - **Decoder**: Generates output step-by-step (used in GPT, T5).

- **Transformer Block**  
  Basic building unit of a Transformer:
  1. Multi-head attention
  2. Add & Layer Norm
  3. Feed-forward network
  4. Add & Layer Norm

- **Feed-Forward Network (FFN)**  
  Applies two linear transformations with activation (ReLU/GELU) in between to each token individually.

- **Residual Connection**  
  Adds input back to the output of a layer to maintain signal and improve gradient flow.

- **Layer Normalization**  
  Normalizes token representations across features to stabilize and accelerate training.

- **Stacking Layers**  
  Deep models (e.g., GPT-3 with 96 transformer blocks) are created by stacking multiple transformer layers.

---

## 🔹 Training Concepts

- **Gradient Flow**  
  Describes how error gradients propagate backward during training.  
  Healthy gradient flow is essential to model convergence.

- **Normalization (General)**  
  Preprocessing step to standardize inputs (text lowercasing, punctuation removal) or features (z-score scaling).

---

## 📘 Summary Table

| Concept                  | Description |
|---------------------------|-------------|
| **Tokenization**          | Splitting raw text into subword tokens |
| **Static Vectors**        | Fixed embeddings (e.g., Word2Vec) |
| **Contextual Vectors**    | Embeddings vary with context (e.g., BERT) |
| **Positional Encoding**   | Injects word order into input |
| **Self-Attention**        | Words attend to other words in the input |
| **Q / K / V**             | Compute attention scores and outputs |
| **Attention Score**       | Importance of one token to another |
| **Multi-Head Attention**  | Parallel attention computations |
| **Masking**               | Prevents attending to future/padding tokens |
| **Transformer Block**     | Basic unit with attention + FFN |
| **Residual Connection**   | Adds input to output to aid training |
| **Layer Norm**            | Normalizes activations to stabilize learning |
| **Gradient Flow**         | Movement of gradients during backprop |
| **Stacking Layers**       | Builds depth and model capacity |

---

## 📂 License

This reference is open-source. Feel free to use or modify in your own Transformer-related projects!

---
