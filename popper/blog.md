---
layout: default
title: Log
description: "PKT research log — a Popperian falsification diary documenting conjectures, corrections, and ideas that turned out to be wrong."
---

# Research Log

In the spirit of Popper, this log records not just what I learn, but what I previously believed that turned out to be wrong. A theory that cannot be falsified is not scientific — and a research log that only records successes is not honest.

---

### [2025-12-21] Initial Formulation
- Defined the "Popper's Knowledge Tensor" framework.
- **Goal:** Move beyond purely inductive learning by integrating deductive falsification.
- **Open question:** How do we mathematically define the "pressure" a deductive rule applies to an inductive pillar?
- **Next step:** Set up the GitHub Pages site and survey existing neuro-symbolic research.

---

### [2025-01] Terminology Corrections

**Falsified: "Masked Learning."** I had been using "Masked Learning" as a catch-all term for what current AI does. This is inaccurate. Masked language modeling (BERT-style) is *one* form of self-supervised learning, but the dominant paradigm in LLMs is autoregressive next-token prediction. The correct general term is **self-supervised learning**, which encompasses masked modeling, autoregressive modeling, contrastive learning, and other objectives.

**Falsified: "Hegelian Episteme."** Earlier drafts conflated two distinct concepts:
- **Hegel's dialectic** (thesis → antithesis → synthesis): describes *how* knowledge develops through contradiction.
- **Foucault's episteme**: describes *the frame* within which knowledge makes sense — the unquestioned assumptions of an era.

These are both relevant to PKT but for different reasons. Hegel's dialectic maps to the induction → falsification → refinement cycle. Foucault's episteme raises questions about whether the rule set $\mathcal{R}$ is universal or contingent. Conflating them weakened the argument by making it seem like the framework was philosophically muddled.

---

### [2025-01] Landscape Discovery

Surveying the neuro-symbolic literature revealed that PKT's unique contribution is narrower than I initially thought:
- **Logic Tensor Networks** already integrate logic with tensors (via fuzzy logic).
- **NeurASP** already enforces hard constraints (via ASP solvers).
- **Constitutional AI** already applies deductive rules to AI behavior.

What remains novel: **hard falsification at the representation level**. Existing systems apply constraints at the loss function (soft) or at the I/O boundary (hard but external). PKT proposes applying hard constraints *directly on internal representations*. This is a genuine gap, but it's a narrower claim than "first framework combining Popper and AI."

---

### [2025-01] Formalization Attempt

Attempting to write down the Falsification Operator $\mathcal{F}$ revealed a core technical problem: **hard thresholding is not differentiable**. This creates a fundamental tension with gradient-based training.

Three candidate resolutions identified:
1. Straight-through estimators (approximate gradients)
2. Alternating optimization (separate inductive and deductive steps)
3. Smooth sigmoid approximation (but this compromises the "hard" claim)

**Current assessment:** Option 2 (alternating optimization) is most promising. It preserves the hard falsification property while being compatible with neural training — similar to how EM algorithms alternate between expectation and maximization steps.

**Falsified: "Just add a penalty term."** My initial instinct was to add a falsification penalty to the loss function. But this makes PKT equivalent to existing soft-constraint approaches (LTNs with a high penalty weight). The whole point of PKT is that falsification is *hard*, not *expensive*. The loss function version is a useful training aid, but the hard operator $\mathcal{F}$ applied between epochs is the actual contribution.

---

### [2025-02] Blog Restructuring

Expanded the blog from 4 pages (~60 lines) to 7 pages (~600 lines). The restructuring was driven by three realizations:
1. The original content was too high-level — it stated claims without grounding them in existing work or formal definitions.
2. The philosophical foundations needed to be separated properly (Popper ≠ Hegel ≠ Foucault).
3. The work needed to position itself honestly within the existing neuro-symbolic landscape.

The blog now maps to a future paper: Overview → Abstract, Motivation → Intro, Philosophy → Background, Landscape → Related Work, Framework → Method, Questions → Discussion.

---

## What's Next

- [ ] Implement a toy PKT system: small tensor, handful of rules, synthetic data. Test whether alternating optimization converges.
- [ ] Prove or disprove the convergence conjecture for a simplified case (e.g., rank-1 tensor with linear rules).
- [ ] Write up the landscape comparison as a standalone related-work section suitable for arXiv submission.
- [ ] Investigate connection to **Popper** (the ILP system by Cropper & Muggleton) — can their hypothesis pruning approach be adapted to continuous tensors?
