---
layout: default
title: Framework
---

# Formal Framework

> **Disclaimer:** The definitions below are **proposed and speculative**. They represent the current best formulation of PKT's core ideas, not proven results. Where something is a conjecture rather than a theorem, it is labeled as such.

---

## 1. The Knowledge Tensor

**Definition.** The *Knowledge Tensor* at time $t$ is a multidimensional array:

$$\mathcal{T}^{(t)} \in \mathbb{R}^{d_1 \times d_2 \times \cdots \times d_n}$$

where each mode (dimension) represents a distinct aspect of knowledge:

| Mode | Interpretation | Example |
|------|---------------|---------|
| $d_1$ | Concepts / entities | "electron," "gravity," "Paris" |
| $d_2$ | Relations / predicates | "is-a," "causes," "located-in" |
| $d_3$ | Confidence / belief strength | $[0, 1]$ — how strongly the relation is held |
| $d_4$ | Temporal context | When the belief was formed or applies |
| $d_5, \ldots, d_n$ | Additional structure | Modality, source, abstraction level |

Each entry $\mathcal{T}^{(t)}\_{i\_1, i\_2, \ldots, i\_n}$ represents the **belief strength** for a specific knowledge claim — e.g., "the concept *electron* stands in the relation *has-charge* with confidence 0.97 in the context of *quantum mechanics*."

This is deliberately more expressive than a knowledge graph (which is a rank-2 adjacency matrix) or a knowledge base (which stores discrete facts). The tensor captures **graded, structured, multi-relational knowledge**.

---

## 2. Inductive Learning

The inductive process builds $\mathcal{T}$ from data. Given a dataset $\mathcal{D}$, the model learns parameters $\theta$ that populate the tensor:

$$\mathcal{T}^{(t)} = f_\theta(\mathcal{D})$$

where $f_\theta$ is a neural encoder (e.g., a transformer or graph neural network). The inductive loss encourages the tensor to faithfully represent the data:

$$\mathcal{L}_{\text{inductive}}(\theta) = -\mathbb{E}_{x \sim \mathcal{D}} \left[ \log p_\theta(x) \right]$$

This is standard — any self-supervised or supervised objective fits here. The key point is that inductive learning alone produces a tensor that reflects statistical patterns in $\mathcal{D}$, including any biases, correlations, or outright falsehoods present in the data.

---

## 3. The Falsification Operator

**Definition.** The *Falsification Operator* is a function:

$$\mathcal{F}: \mathbb{R}^{d_1 \times \cdots \times d_n} \times \mathcal{R} \rightarrow \mathbb{R}^{d_1 \times \cdots \times d_n}$$

where $\mathcal{R}$ is a set of **deductive rules**. The operator takes a Knowledge Tensor and a rule set, and returns a *pruned* tensor:

$$\mathcal{T}' = \mathcal{F}(\mathcal{T}, \mathcal{R})$$

**Proposed semantics.** For each rule $r \in \mathcal{R}$ and each tensor entry, $\mathcal{F}$ checks whether the entry is consistent with $r$. If not, the entry is **projected to zero**:

$$\mathcal{F}(\mathcal{T}, \mathcal{R})\_{i\_1, \ldots, i\_n} = \begin{cases} \mathcal{T}\_{i\_1, \ldots, i\_n} & \text{if } \forall r \in \mathcal{R}: \text{consistent}(\mathcal{T}\_{i\_1, \ldots, i\_n}, r) \\\\ 0 & \text{otherwise} \end{cases}$$

This is a **hard** operation — not a soft penalty. Entries that violate deductive rules are eliminated, not merely discouraged.

### What counts as a "rule"?

Rules in $\mathcal{R}$ could include:
- **Logical constraints:** $\forall x: \text{mammal}(x) \Rightarrow \text{vertebrate}(x)$
- **Physical laws:** Conservation of energy, transitivity of ordering relations
- **Ontological constraints:** An entity cannot belong to mutually exclusive categories
- **Consistency requirements:** $P(A) + P(\neg A) = 1$

The rule set is **externally provided**, not learned. This is a deliberate design choice: the rules represent the *deductive* component of knowledge, which in the Popperian framework comes from theory, not from data.

### Open problem: differentiability

The falsification operator as defined above is **not differentiable** — it involves a hard threshold (zero out or keep). This creates a tension with gradient-based training. Three possible resolutions:

1. **Straight-through estimator:** Use the hard operator in the forward pass but approximate gradients in the backward pass (Bengio et al., 2013).
2. **Alternating optimization:** Alternate between gradient-based inductive steps and non-differentiable falsification steps (similar to EM algorithms).
3. **Smooth approximation:** Replace the hard threshold with a steep sigmoid, making $\mathcal{F}$ approximately differentiable. *But this compromises the "hard falsification" claim* — it becomes a soft constraint with a very high penalty, which is what existing systems already do.

This is the **central technical challenge** of PKT. Resolution 2 (alternating optimization) is the most promising, as it preserves the hard falsification property while remaining compatible with neural training.

---

## 4. Tensor Decomposition as Pruning

After falsification, the tensor $\mathcal{T}'$ may be sparse and noisy. **Tensor decomposition** provides a principled way to extract the essential structure.

The **CP decomposition** (Hitchcock, 1927; Kolda & Bader, 2009) approximates a tensor as a sum of rank-one components:

$$\mathcal{T}' \approx \sum_{k=1}^{R} \lambda_k \, \mathbf{a}_k^{(1)} \otimes \mathbf{a}_k^{(2)} \otimes \cdots \otimes \mathbf{a}_k^{(n)}$$

where $R$ is the rank, $\lambda_k$ are weights, and $\mathbf{a}_k^{(j)}$ are factor vectors. Choosing a low rank $R$ forces the decomposition to retain only the **dominant patterns**, discarding noise and hallucination.

**Conjecture.** Low-rank decomposition of the falsified tensor $\mathcal{T}'$ produces a representation that is both *logically consistent* (by construction, since inconsistent entries were zeroed) and *statistically parsimonious* (by the rank constraint). This combination may be a useful formal definition of "knowledge" — structured belief that has survived both empirical and logical tests.

---

## 5. The Combined Loss Function

The full PKT training objective combines inductive and falsification losses:

$$\mathcal{L} = \mathcal{L}_{\text{inductive}} + \lambda \, \mathcal{L}_{\text{falsification}}$$

where:

- $\mathcal{L}\_{\text{inductive}}$ is the standard data likelihood (as above).
- $\mathcal{L}\_{\text{falsification}}$ penalizes entries that would be zeroed by $\mathcal{F}$:

$$\mathcal{L}_{\text{falsification}} = \sum_{i_1, \ldots, i_n} \mathcal{T}_{i_1, \ldots, i_n}^2 \cdot \mathbb{1}\left[\neg \text{consistent}(\mathcal{T}_{i_1, \ldots, i_n}, \mathcal{R})\right]$$

- $\lambda > 0$ controls the trade-off between fitting the data and obeying the rules.

**Note:** This loss function is a **soft approximation** of the hard falsification operator. In practice, training would likely use this differentiable loss, with periodic applications of the hard operator $\mathcal{F}$ to enforce strict consistency. The interplay between soft guidance (during gradient steps) and hard enforcement (between epochs) is a key area for future work.

---

## 6. The Learning Cycle

Putting it all together, PKT proposes an iterative learning process:

**Step 1. Induction.** Learn $\mathcal{T}^{(t)}$ from data by minimizing $\mathcal{L}$.

**Step 2. Falsification.** Apply $\mathcal{F}$ to get $\mathcal{T}'^{(t)} = \mathcal{F}(\mathcal{T}^{(t)}, \mathcal{R})$.

**Step 3. Decomposition.** Compute low-rank approximation of $\mathcal{T}'^{(t)}$ to extract core structure.

**Step 4. Refinement.** Use the decomposed tensor as initialization for the next inductive step.

**Repeat** until convergence.

**Convergence Conjecture.** *Under suitable conditions on $\mathcal{R}$ and $\mathcal{D}$, the iteration above converges to a fixed point $\mathcal{T}^*$ that is both statistically faithful to $\mathcal{D}$ and logically consistent with $\mathcal{R}$.*

This conjecture is **unproven**. Conditions for convergence likely require:
- The rule set $\mathcal{R}$ is consistent (no contradictory rules).
- The data $\mathcal{D}$ is not completely at odds with $\mathcal{R}$ (some feasible solution exists).
- The learning rate and falsification schedule are appropriately tuned.

Proving (or disproving) this conjecture is the most important theoretical milestone for PKT.

---

---

## References

- Bengio, Y., Léonard, N. & Courville, A. (2013). Estimating or Propagating Gradients Through Stochastic Neurons for Conditional Computation. [arXiv:1308.3432](https://arxiv.org/abs/1308.3432)
- Hitchcock, F.L. (1927). The Expression of a Tensor or a Polyadic as a Sum of Products. *Journal of Mathematics and Physics*, 6(1–4), 164–189.
- Kolda, T.G. & Bader, B.W. (2009). Tensor Decompositions and Applications. *SIAM Review*, 51(3), 455–500.

---

*Next: [Open Questions](./questions) — the deeper philosophical puzzles this framework raises.*
