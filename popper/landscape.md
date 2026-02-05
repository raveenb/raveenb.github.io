---
layout: default
title: Landscape
description: "Survey of neuro-symbolic AI — Logic Tensor Networks, DeepProbLog, NeurASP, Constitutional AI, Neural Theorem Provers — and how PKT's hard falsification differs."
---

# The Neuro-Symbolic Landscape

PKT does not exist in a vacuum. The idea of combining neural learning with logical reasoning has a rich history. This page surveys the major approaches, identifies what each does well, and clarifies where PKT proposes something different.

---

## Existing Approaches

### Logic Tensor Networks (LTNs)
**Badreddine et al., 2022** ([arXiv:2012.13635](https://arxiv.org/abs/2012.13635))

LTNs ground first-order logic in real-valued tensor computations. Logical predicates become differentiable functions, and logical connectives (AND, OR, NOT) are approximated via fuzzy logic operators (typically the product t-norm). A "satisfaction" score measures how well a model's outputs conform to a set of logical axioms, and this score is maximized during training.

**Strength:** Elegant integration — logic becomes part of the loss function, making the whole system end-to-end differentiable.
**Limitation:** The logic is *fuzzy*. A statement can be "70% true." This is useful for soft constraints but cannot enforce hard logical requirements. A model can learn to satisfy axioms approximately while still violating them in specific cases.

### DeepProbLog
**Manhaeve et al., 2018** ([arXiv:1805.10872](https://arxiv.org/abs/1805.10872))

DeepProbLog extends ProbLog (a probabilistic logic programming language) with neural predicates. Neural networks provide probabilistic facts that feed into logical inference. The system supports exact probabilistic inference over logical programs that include neural components.

**Strength:** Principled probabilistic semantics. The combination of neural perception and logical reasoning is mathematically well-founded.
**Limitation:** Scalability. Exact inference is exponential in the worst case. The logical component must be relatively small and well-structured.

### NeurASP
**Yang et al., 2020** ([arXiv:2307.07700](https://arxiv.org/abs/2307.07700))

NeurASP integrates neural networks with Answer Set Programming (ASP). Neural outputs become probabilistic inputs to an ASP solver, which enforces hard logical constraints. The ASP solver's output is used to compute gradients for training the neural component.

**Strength:** Hard constraints — ASP is a constraint satisfaction framework, so logical rules are *enforced*, not merely encouraged.
**Limitation:** The neural and logical components are coupled at the interface, not integrated at the representation level. The neural net learns to produce inputs the ASP solver can use, but the internal representations are not themselves logically structured.

### Constitutional AI (CAI)
**Bai et al., 2022** ([arXiv:2212.08073](https://arxiv.org/abs/2212.08073))

Anthropic's Constitutional AI applies deductive-style rules (a "constitution") to constrain model behavior. The model critiques and revises its own outputs based on a set of principles, then is fine-tuned on the revisions via RLHF.

**Strength:** Practical and deployable. Constitutional AI has been used to train production models with measurably improved safety.
**Limitation:** The constitution governs *behavior*, not *knowledge*. The model's internal representations remain unconstrained — it may "know" something is wrong but say it anyway if the behavioral constraints don't cover that case.

### Neural Theorem Provers (NTPs)
**Rocktäschel & Riedel, 2017** ([arXiv:1705.11040](https://arxiv.org/abs/1705.11040))

NTPs make theorem proving differentiable. Logical unification is replaced with a soft matching operation over vector representations, allowing backpropagation through proof steps. The system can learn to perform logical inference end-to-end.

**Strength:** Makes deduction itself learnable. The system can generalize beyond the explicitly given rules.
**Limitation:** The "proofs" are approximate. Soft unification means the system can produce "proofs" of statements that are not logically valid.

---

## Existing Popper + AI Work

PKT is not the first project to connect Popper to machine learning:

- **Cropper & Muggleton, 2016** ([arXiv:1704.08111](https://arxiv.org/abs/1704.08111)) developed an Inductive Logic Programming (ILP) system literally named "Popper" that uses hypothesis testing and pruning — generating candidate logic programs and using failed examples to constrain the search space.
- **Hocquette & Muggleton, 2020** formalized *learning from failures* in ILP, directly operationalizing Popperian epistemology.
- **Schmidhuber's work on curiosity-driven learning** (2010) implements a form of conjecture-testing, where an agent actively seeks experiences that falsify its current world model.

These are important precursors. PKT differs in operating at the *representation level* (tensors) rather than the *symbolic level* (logic programs), and in proposing a *continuous* falsification process integrated with gradient-based learning.

---

## Where PKT Fits

The key dimension of comparison is **how logic constrains learning**:

| System | Logic Integration | Constraint Type | Representation |
|--------|------------------|----------------|----------------|
| LTNs | Fuzzy logic in loss function | Soft (differentiable penalty) | Tensor |
| DeepProbLog | Probabilistic logic programming | Soft (probabilistic) | Symbolic + neural |
| NeurASP | ASP solver at interface | Hard (at output) | Symbolic + neural |
| Constitutional AI | Natural language rules | Soft (behavioral) | Latent (LLM internals) |
| NTPs | Differentiable unification | Soft (approximate proofs) | Vector |
| **PKT (proposed)** | **Falsification operator** | **Hard (at representation)** | **Tensor** |

The distinguishing claim of PKT:

> **Existing systems apply logical constraints at the loss function level (soft) or at the input/output interface (hard but external). PKT proposes applying hard constraints at the representation level — directly on the Knowledge Tensor.**

This means:
1. **Not just penalizing** inconsistency (like LTNs) but **eliminating** it via a projection operator.
2. **Not just filtering outputs** (like NeurASP or CAI) but **structuring internal representations** so that inconsistent states cannot persist.
3. **Not replacing** neural learning with logic but **integrating** falsification into the representation itself.

Whether this is achievable is an open question. The [Framework](./math) page attempts a formal definition; the [Open Questions](./questions) page acknowledges what remains unresolved.

---

---

## References

- Badreddine, S. et al. (2022). Logic Tensor Networks. [arXiv:2012.13635](https://arxiv.org/abs/2012.13635)
- Manhaeve, R. et al. (2018). DeepProbLog: Neural Probabilistic Logic Programming. [arXiv:1805.10872](https://arxiv.org/abs/1805.10872)
- Yang, Z. et al. (2020). NeurASP: Embracing Neural Networks into Answer Set Programming. [arXiv:2307.07700](https://arxiv.org/abs/2307.07700)
- Bai, Y. et al. (2022). Constitutional AI: Harmlessness from AI Feedback. [arXiv:2212.08073](https://arxiv.org/abs/2212.08073)
- Rocktäschel, T. & Riedel, S. (2017). End-to-End Differentiable Proving. [arXiv:1705.11040](https://arxiv.org/abs/1705.11040)
- Cropper, A. & Muggleton, S. (2016). Learning Higher-Order Logic Programs through Abstraction and Invention. [arXiv:1704.08111](https://arxiv.org/abs/1704.08111)
- Schmidhuber, J. (2010). Formal Theory of Creativity, Fun, and Intrinsic Motivation. *IEEE Transactions on Autonomous Mental Development*, 2(3), 230–247.

---

*Next: [Formal Framework](./math) — definitions, operators, and a proposed loss function.*
