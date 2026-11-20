---
layout: note
title: Understanding Transformer Architecture
description: Self-attention mechanism, multi-head attention, and positional encodings.
category: self-study
date: 2026-11-20
tags: [machine-learning, deep-learning, nlp, transformers]
pdf: /assets/pdf/example_pdf.pdf
tex: /assets/tex/transformer-architecture.tex
---

## Key Concepts

The Transformer architecture (Vaswani et al., 2017) eliminated recurrence in sequence modeling in favor of pure attention mechanisms.

### Scaled Dot-Product Attention

The core attention calculation is defined as:

$$\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V$$

Where:
- $Q \in \mathbb{R}^{n \times d_k}$ is the Query matrix
- $K \in \mathbb{R}^{m \times d_k}$ is the Key matrix
- $V \in \mathbb{R}^{m \times d_v}$ is the Value matrix
- $\sqrt{d_k}$ acts as a scaling factor to prevent vanishing gradients in the softmax.

### Multi-Head Attention

Instead of performing a single attention function, Queries, Keys, and Values are linearly projected $h$ times with different learned parameter matrices:

$$\text{MultiHead}(Q, K, V) = \text{Concat}(\text{head}_1, \dots, \text{head}_h)W^O$$

Where $\text{head}_i = \text{Attention}(Q W_i^Q, K W_i^K, V W_i^V)$.

### Positional Encoding

Because Transformers process tokens in parallel without sequential order, positional encodings are injected into input embeddings using sinusoidal functions:

$$PE_{(pos, 2i)} = \sin\left(\frac{pos}{10000^{2i/d_{\text{model}}}}\right)$$
$$PE_{(pos, 2i+1)} = \cos\left(\frac{pos}{10000^{2i/d_{\text{model}}}}\right)$$
