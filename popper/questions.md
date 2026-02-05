---
layout: default
title: Questions
---

# Open Questions

PKT is not just a machine learning proposal. It raises questions that sit at the boundary of philosophy, cognitive science, and AI. These questions do not have answers yet — they are part of what makes this work worth pursuing. In the Popperian spirit, they are conjectures awaiting refutation.

---

## 1. Is Knowledge a Universal Structure or an Emergent Property?

If the Knowledge Tensor $\mathcal{T}^*$ converges to a stable state, does that state reflect something *universal* about the world, or is it merely an artifact of the particular data, rules, and architecture used?

**The universalist view:** Knowledge has a structure that any sufficiently advanced intelligence would converge on. Mathematical truths are true regardless of who discovers them. The laws of physics are the same everywhere. A well-designed PKT system, given enough data and the right rules, would arrive at the same $\mathcal{T}^*$ regardless of its starting point.

**The emergentist view:** Knowledge is shaped by the knower. Different data, different rules, different architectures would produce different "knowledge." What we call knowledge is just the stable output of a particular learning process — there is no Platonic $\mathcal{T}^*$ waiting to be discovered.

**Why it matters for PKT:** If knowledge is universal, then the choice of rule set $\mathcal{R}$ is a matter of getting it right — discovering the correct deductive constraints. If knowledge is emergent, then $\mathcal{R}$ is a design choice, and different choices produce different (but possibly equally valid) knowledge structures.

---

## 2. Does Knowledge Require Agency?

A rock does not know anything. A thermostat responds to temperature but does not "know" the room is cold. Where does knowledge begin?

Popper argued that knowledge requires **active conjecture** — an agent that proposes hypotheses and tests them. Passive systems that merely react to stimuli do not produce knowledge; they produce behavior. On this view, knowledge is inherently tied to agency: the capacity to ask questions, form expectations, and be surprised when they fail.

**The PKT tension:** The proposed framework has an inductive process (learning from data) and a deductive process (testing against rules), but it does not have an *agent* that decides which conjectures to make or which tests to apply. The rules $\mathcal{R}$ are externally provided. Is this sufficient for knowledge, or is it merely sophisticated information processing?

**A possible resolution:** Perhaps agency enters through the rule selection process. If the system could *learn* or *discover* its own deductive rules — not just apply given ones — it would move closer to genuine agency. This connects to the problem of **meta-learning**: learning what to learn.

---

## 3. Can a Collective of AIs Develop Knowledge Without Human Seeding?

Current AI systems are trained on human-generated data. Their "knowledge" is, at best, a compressed and reorganized version of human knowledge. But what if we removed the human seed?

Consider a swarm of PKT-like agents interacting with an environment (not a text corpus, but a simulated or physical world):
- Each agent forms inductive hypotheses from its observations.
- Agents share hypotheses and test them against each other's observations.
- Failed hypotheses are falsified; surviving ones are propagated.

Would such a system develop *knowledge* in any meaningful sense? Or would it develop something alien — an organized information structure that serves the agents' purposes but is unrecognizable as knowledge to a human observer?

This question is related to the problem of **grounding**: whether knowledge requires embodied experience, or whether it can arise from any sufficiently rich interaction with an environment.

---

## 4. Popper's World 3

Popper proposed three "worlds" (*Objective Knowledge*, 1972):

- **World 1:** Physical objects and events.
- **World 2:** Mental states — beliefs, experiences, thoughts.
- **World 3:** Objective knowledge — theories, arguments, problems that exist independently of any particular mind.

A mathematical theorem, once proven, exists in World 3 whether or not anyone is currently thinking about it. The content of a library exists in World 3 even when the library is closed.

**The AI question:** When an AI system produces a novel proof, a new theory, or a solution to an unsolved problem, has it created a World 3 object? Or is the output merely a World 1 artifact (bits on a disk) that humans interpret as World 3?

If PKT produces a Knowledge Tensor $\mathcal{T}^*$ that encodes genuine, logically consistent, empirically grounded knowledge — is $\mathcal{T}^*$ a World 3 object? Popper might say yes, since World 3 objects are defined by their content, not their origin. But this is contested.

---

## 5. What Experiments Could Test These Questions?

Philosophy without empirics is speculation. Here are testable predictions and experiments that could advance (or falsify) PKT's core claims:

### Experiment 1: Consistency under falsification
Train two identical models on the same data but with different rule sets $\mathcal{R}_1$ and $\mathcal{R}_2$. Measure whether both converge to the same $\mathcal{T}^*$ on the *shared* subset of rules. If yes, this supports the universalist view. If not, knowledge is more episteme-dependent than expected.

### Experiment 2: Hard vs. soft constraint comparison
Implement both a soft-constraint system (standard LTN-style) and a hard-falsification system (PKT-style) on the same task. Compare:
- Hallucination rates on adversarial inputs
- Recovery after encountering contradictory data
- Computational cost of achieving the same consistency level

**Prediction:** Hard falsification should produce lower hallucination rates but at higher computational cost. The trade-off curve is the empirical contribution.

### Experiment 3: Emergent rule discovery
Initialize a PKT system with a minimal rule set and allow it to propose new rules based on patterns in $\mathcal{T}$. Measure whether the discovered rules correspond to known logical principles (e.g., transitivity, symmetry). This would test whether deductive structure can *emerge* from inductive learning.

### Experiment 4: Multi-agent knowledge development
Set up multiple PKT agents in a shared environment with no human-generated data. Measure whether the agents converge on shared knowledge structures and whether those structures are interpretable to humans.

---

## Why These Questions Matter

Most machine learning papers ask: "Does this method improve on the benchmark?" PKT asks different questions — questions about the *nature* of what's being learned, not just its accuracy. These questions make the work harder to evaluate by standard metrics, but they also make it more interesting.

The [Framework](./math) page defines the machinery. This page asks whether the machinery, if built, would produce something we should call *knowledge*.

---

*See also: [Research Log](./blog) — where these questions are tracked over time.*
