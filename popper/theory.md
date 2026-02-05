---
layout: default
title: Philosophy
---

# Philosophical Foundations

PKT draws on three distinct philosophical traditions. Each contributes a different piece of the puzzle, and it is important to keep them separate — earlier drafts of this work conflated Hegel and Foucault, which muddied the argument. This page corrects that.

---

## Popper's Falsificationism

Karl Popper's central insight is deceptively simple: **we cannot prove a theory true; we can only fail to falsify it.** Knowledge does not grow by accumulating confirmations. It grows by *conjecture and refutation* — proposing bold hypotheses and subjecting them to the harshest tests we can devise (Popper, *The Logic of Scientific Discovery*, 1934/1959).

A theory that cannot be falsified is not scientific. "All swans are white" is scientific because observing a black swan would refute it. "Everything happens for a reason" is not, because no observation could count against it.

### Why This Matters for AI

Current neural networks are **confirmation machines**. They learn from data by adjusting weights to maximize likelihood — to confirm that the training distribution is well-modeled. There is no mechanism for *refutation*. If a model learns an incorrect association (e.g., "all swans mentioned in the training data are white"), no internal process challenges that belief.

PKT proposes to add a falsification mechanism: a deductive operator that tests inductively learned representations against logical rules and eliminates those that fail. This is not just a regularizer — it is a structural commitment to the principle that **knowledge must be falsifiable to be meaningful**.

---

## Hegel's Dialectic

Georg Wilhelm Friedrich Hegel described a process by which ideas develop through contradiction:

1. **Thesis** — An initial proposition or state of understanding.
2. **Antithesis** — A contradiction or challenge to the thesis.
3. **Synthesis** — A higher-order resolution that incorporates and transcends both.

This is not a linear process but a spiral — each synthesis becomes a new thesis, generating its own antithesis. Hegel saw this dialectic as the engine of all intellectual progress (*Phenomenology of Spirit*, 1807).

### The PKT Dialectic

In the PKT framework, the dialectic maps directly onto the learning cycle:

| Dialectical Stage | PKT Process |
|-------------------|-------------|
| **Thesis** | Inductive hypothesis — patterns learned from data |
| **Antithesis** | Deductive test — logical rules that challenge the hypothesis |
| **Synthesis** | Refined knowledge — the tensor after falsification and re-learning |

Each iteration of induction → falsification → refinement is a dialectical step. The Knowledge Tensor does not simply accumulate information; it is *transformed* through contradiction. The result is not a compromise between induction and deduction but a higher-order representation that neither could produce alone.

This is what makes PKT more than "neural nets plus logic." It is a framework in which **knowledge emerges from the tension between learning and testing**.

---

## Foucault's Episteme

Michel Foucault used the term *episteme* to describe the underlying framework of assumptions that defines what counts as knowledge in a given era (*The Order of Things*, 1966). The episteme is not a theory but the *conditions of possibility* for theories — the invisible rules that determine which questions can be asked and which answers make sense.

> **Note on terminology:** Earlier drafts of this work used "Hegelian Episteme," conflating Hegel's dialectic with Foucault's episteme. These are distinct concepts. Hegel describes *how* knowledge develops (through contradiction). Foucault describes *the frame* within which knowledge operates (the assumptions we don't question). Both are relevant to PKT, but for different reasons.

### Relevance to PKT

Foucault's concept raises a hard question for any knowledge framework: **Is the Knowledge Tensor universal, or is it episteme-dependent?**

If knowledge is structured by an episteme, then:
- The logical rules used for falsification are themselves products of a particular episteme.
- A PKT system trained within one paradigm might produce "knowledge" that is incoherent in another.
- There may be no view from nowhere — no set of deductive rules that is universally valid.

This is not a flaw to be fixed but a **limitation to be acknowledged**. The rules in the falsification operator $\mathcal{F}$ are not Platonic truths; they are the best rules available within the current episteme. PKT is honest about this: knowledge is *provisional* in two senses — it can be falsified by new data (Popper), and it is framed by assumptions that may themselves shift (Foucault).

---

## The Three Traditions Combined

| Philosopher | Key Concept | Role in PKT |
|------------|-------------|-------------|
| **Popper** | Falsificationism | The *mechanism*: knowledge grows by conjecture and refutation |
| **Hegel** | Dialectic | The *process*: thesis (induction) meets antithesis (deduction) to produce synthesis (refined knowledge) |
| **Foucault** | Episteme | The *frame*: all knowledge, including PKT's rules, operates within contingent assumptions |

Together, these give PKT its philosophical depth. It is not enough to say "add logic to neural nets." We need to understand *why* falsification matters (Popper), *how* contradiction drives progress (Hegel), and *what limits* any knowledge framework faces (Foucault).

---

---

## References

- Popper, K. (1934/1959). *The Logic of Scientific Discovery*. Routledge.
- Hegel, G.W.F. (1807). *Phenomenology of Spirit*. Trans. A.V. Miller, Oxford University Press, 1977.
- Foucault, M. (1966). *The Order of Things: An Archaeology of the Human Sciences*. Trans. Routledge, 1970.

---

*Next: [The Neuro-Symbolic Landscape](./landscape) — what already exists in this space, and how PKT differs.*
