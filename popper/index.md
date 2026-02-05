---
layout: default
title: Overview
description: "Popper's Knowledge Tensor (PKT) — a neuro-symbolic framework proposing hard falsification as an alternative to soft constraint satisfaction in AI."
---

# Popper's Knowledge Tensor (PKT)
**Toward Hard Falsification in Neuro-Symbolic AI**

Modern AI systems learn by induction — absorbing statistical patterns from massive datasets. They are powerful pattern matchers, but they cannot *reject* a hypothesis the way a scientist can. When a large language model hallucinates a plausible-sounding falsehood, there is no internal mechanism that says "this contradicts what I know to be true." The model has no capacity for **falsification**.

PKT proposes a different kind of architecture: one where knowledge is not merely *accumulated* but actively **tested and pruned**. Inspired by Karl Popper's philosophy of science, the framework treats every learned representation as a *conjecture* — provisional until it survives deductive stress tests.

---

## The Core Idea

Most neuro-symbolic approaches (Logic Tensor Networks, DeepProbLog, NeurASP) integrate logic as a **soft constraint**: logical rules nudge the model toward consistency, penalizing violations through differentiable loss terms. The model is *encouraged* to be logical but never *required* to be.

PKT takes a harder line. It proposes a **falsification operator** that *eliminates* representations violating deductive rules, rather than merely penalizing them. The distinction matters:

| Approach | Mechanism | Failure Mode |
|----------|-----------|-------------|
| Soft constraint (existing) | Penalty term in loss function | Model can learn to "pay the penalty" and keep inconsistencies |
| Hard falsification (PKT) | Projection operator zeros out violating entries | Inconsistent representations are structurally impossible |

This is analogous to the difference between a tax on pollution (soft) and a physical filter that removes pollutants (hard).

---

## Roadmap

This blog develops the PKT idea across six threads, each building toward a formal paper:

1. **[Motivation](./motivation)** — Why pure induction isn't enough, and why hallucination is a symptom of a deeper architectural gap.
2. **[Philosophy](./theory)** — The epistemological foundations: Popper's falsificationism, Hegel's dialectic, and the question of what knowledge *is*.
3. **[Landscape](./landscape)** — What already exists in neuro-symbolic AI, and where PKT fits (and differs).
4. **[Framework](./math)** — The formal definition: the Knowledge Tensor, the Falsification Operator, and a proposed loss function.
5. **[Open Questions](./questions)** — The deep questions this work raises about the nature of knowledge, agency, and AI.
6. **[Research Log](./blog)** — A Popperian falsification log: what I've conjectured, tested, and discarded.

---

## Status

This is **active research in progress**. The framework is speculative — definitions are proposed rather than proven, and no experiments have been run yet. The blog is the thinking tool; the paper comes later.

*What you're reading is the conjecture. The refutation is the work ahead.*
