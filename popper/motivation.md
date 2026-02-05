---
layout: default
title: Motivation
---

# The Limits of Pure Induction

## What Current AI Actually Does

The dominant paradigm in modern AI is **self-supervised learning**: a model sees partial data and learns to predict the missing parts. In language models, this means predicting the next token. In vision models (MAE, BEiT), it means reconstructing masked image patches. In contrastive learning (CLIP, SimCLR), it means recognizing that two views of the same data should produce similar representations.

All of these are forms of **induction** — generalizing from observed examples to unobserved ones. The model builds a statistical model of its training distribution and uses that model to fill in gaps. This is Kahneman's **System 1**: fast, intuitive, pattern-based reasoning (Kahneman, *Thinking, Fast and Slow*, 2011).

System 1 is remarkably powerful. Scaling laws show that larger models trained on more data consistently improve on benchmarks (Kaplan et al., [arXiv:2001.08361](https://arxiv.org/abs/2001.08361)). But there is a ceiling, and we are approaching it.

## Diminishing Returns

Three trends suggest that pure induction is insufficient for general intelligence:

1. **Data exhaustion.** We are running out of high-quality text data. Estimates suggest that all publicly available text will be consumed by frontier models within the next few years (Villalobos et al., [arXiv:2211.04325](https://arxiv.org/abs/2211.04325)). Synthetic data helps, but risks model collapse — learning from your own outputs amplifies errors (Shumailov et al., [arXiv:2305.17493](https://arxiv.org/abs/2305.17493)).

2. **Benchmark saturation.** Performance on standard benchmarks improves logarithmically with compute. Each doubling of resources yields smaller gains. The "last mile" problems — multi-step reasoning, mathematical proof, causal inference — resist brute-force scaling.

3. **Hallucination persistence.** Despite extensive RLHF and safety tuning, language models continue to produce confident falsehoods. Crucially, hallucination rates do not decrease proportionally with model size (Ji et al., [arXiv:2202.03629](https://arxiv.org/abs/2202.03629)). This suggests hallucination is **structural**, not merely a data quality issue.

## Hallucination as a Symptom

Why do models hallucinate? The standard answer is "they generate plausible continuations based on training statistics." But this frames hallucination as an accident. A deeper framing:

> **Hallucination is what happens when a system has induction but no falsification.**

A scientist who forms a hypothesis from data (induction) and never tests it against established laws (deduction) will produce plausible-sounding theories that happen to be wrong. That is exactly what an LLM does. It has no mechanism to ask: *"Does this output contradict something I know to be true?"*

Current mitigations — retrieval-augmented generation, chain-of-thought prompting, self-consistency checks — are patches. They improve reliability without addressing the architectural gap: **there is no deductive module in the system**.

## System 1 Needs System 2

Kahneman's framework maps cleanly onto this problem:

| | System 1 (Inductive) | System 2 (Deductive) |
|-|---------------------|---------------------|
| **Human cognition** | Pattern recognition, intuition | Logical reasoning, verification |
| **Current AI** | Self-supervised learning, neural nets | *Missing* |
| **PKT proposal** | Knowledge Tensor built from data | Falsification Operator applying logical rules |

Human intelligence is not just pattern matching. It is pattern matching **plus** the ability to check those patterns against rules, reject inconsistencies, and revise beliefs. The extraordinary effectiveness of human cognition comes from the interplay between these two systems.

Current AI has System 1 in abundance. PKT proposes to add System 2.

## The Gap

What's missing is a mechanism for **falsification** — a process that takes inductively learned representations and subjects them to deductive tests. Not a soft penalty that discourages inconsistency, but a hard operator that *eliminates* it.

This is the gap that PKT aims to fill. The next pages develop the philosophical foundations for why falsification matters ([Philosophy](./theory)), survey what already exists in this space ([Landscape](./landscape)), and propose a formal framework for how it could work ([Framework](./math)).
