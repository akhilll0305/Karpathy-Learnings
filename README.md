# 🚀 LLM Engineering Journey – From Scratch Implementations

## 📌 Overview

This repository documents my hands-on journey into understanding **Large Language Models (LLMs)** from first principles.

Instead of relying on high-level libraries blindly, this repo focuses on building core components manually to deeply understand:

- Self-attention
- Transformer blocks
- GPT architecture
- Tokenization
- Training loops
- Loss functions
- Scaling behavior

This learning path is inspired by:

- Andrej Karpathy's educational videos
- The original Transformer paper: *Attention Is All You Need*

---

## 📂 Repository Structure

```bash
Karpathy-Learnings/
│
├── README.md
│
├── Build GPT/
│   ├── bigram.py
│   ├── gpt.py
│   ├── input.txt
│   └── more.txt
│
└── GPT Tokenizer/   # 🚧 In progress
```

---

## 📖 Modules

### 1️⃣ `Build GPT/`

Implementation of a GPT-style decoder-only Transformer from scratch in PyTorch.

#### 📚 Covers

- Bigram language model
- Self-attention
- Multi-head attention
- Transformer block
- LayerNorm (Pre-LN vs Post-LN understanding)
- Residual connections
- Causal masking
- Training loop
- Text generation

#### 🧠 Key Learning Outcomes

- How autoregressive modeling works
- How masked attention enforces causality
- Why residual connections stabilize training
- Why modern LLMs use Pre-LN
- How logits → softmax → cross-entropy loss works

---

### 2️⃣ `tokenizer/` *(Next Phase 🚧)*

Planned implementation based on Karpathy's tokenizer deep dive.

#### 📚 Will Cover

- Byte Pair Encoding (BPE)
- Vocabulary construction
- Merge rules
- Encoding & decoding
- Token distribution analysis

#### 🎯 Goal

Understand how raw text becomes model-consumable tokens.

---

## 🧠 Core Concepts Understood

### 🔹 Self-Attention

Tokens dynamically weigh relevance of previous tokens using:

$$\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d}}\right)V$$

### 🔹 Causal Masking

Prevents a token from attending to future tokens during training and generation.

### 🔹 Transformer Block

> Communication → Computation → Stabilization

```
LayerNorm
   ↓
Self-Attention
   ↓
Residual Add
   ↓
LayerNorm
   ↓
FeedForward
   ↓
Residual Add
```

### 🔹 Decoder-Only Architecture

Used in GPT-style models:

- Masked self-attention
- No encoder
- Autoregressive generation
- Next-token prediction objective

---

## 🔬 Future Additions

- [ ] Tokenizer implementation
- [ ] FlashAttention exploration
- [ ] RoPE positional embeddings
- [ ] Multi-Query Attention
- [ ] Scaling experiments
- [ ] Small-scale pretraining experiments

---

## 📈 Why This Repository Exists

This repository is not just code — it is a structured learning archive.

The goal is to:

- Move from **user** of LLMs → **builder** of LLMs
- Understand architectural evolution
- Build intuition for modern systems
- Develop implementation-level clarity

---

## 📌 Long-Term Vision

Build towards:

- Training small LLMs from scratch
- Understanding modern improvements
- Evaluating model behavior
- Implementing research papers

---

## 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Primary language |
| PyTorch | Deep learning framework |
| Minimal external deps | Keep it from scratch |

---

## ✍️ Author Notes

This repository is continuously evolving as I explore deeper into LLM architecture, optimization techniques, and tokenizer design.