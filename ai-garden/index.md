---
layout: default
title: AI in the Garden
description: "From plant diagnostics to micro-drones — exploring what happens when AI moves from the digital world into the soil, weather, and living systems of a real garden."
---

# AI in the Garden
**What happens when artificial intelligence meets living things**

![A lush garden with dozens of species, overlaid with gentle digital diagnostic readings](/assets/images/ai-garden/hero.jpg)

---

## Fifty Species, Fifty Personalities

I have been gardening for a while. Not casually — I maintain something like fifty species of plants across multiple levels of a terraced garden. Flowering shrubs, fruit trees, ferns, succulents, herbs, creepers. Each one has preferences. Personalities, if you'll allow the word.

Some plants love one corner of the garden and sulk in another. One species drops its leaves on the lower terrace while a closely related species — mere meters away, in apparently identical conditions — pushes out flowers. The difference might be drainage. It might be three hours less afternoon sun. It might be the pH of the soil in that specific patch, or the root competition from a nearby tree, or something I haven't thought of.

A garden with fifty species is a complex system. It has microclimates, symbiotic relationships, competitive dynamics, seasonal rhythms, and failure modes that cascade in unexpected ways. And for a long time, I had no one to discuss the *specific, local, contextual* questions with. Gardening books give general advice. YouTube gives popular advice. Neither knows about *my* garden.

---

## AI as Consultant

This is where Claude entered the picture, and the results have been genuinely useful.

The conversation is different from what you'd get from a book or a search engine. I can describe a *specific* situation — "my frangipani on the upper level is dropping leaves, but the one on the lower level is fine; the upper level gets more afternoon sun and the soil drains faster" — and get a diagnostic response that accounts for the *combination* of factors. Not just "frangipanis drop leaves in winter" but a differential analysis: could be dormancy (normal), could be overwatering stress if the lower one has better drainage than I think, could be a fungal issue exacerbated by the afternoon heat.

What's been most valuable:

- **Soil testing guidance.** Claude suggested testing pH and mineral content at different levels of the garden after I described inconsistent growth patterns. The results revealed significant pH variation — more acidic at the lower terrace (where water collects) and more alkaline higher up. This explained several mysteries at once.
- **Leaf diagnostics.** Describing leaf color changes, spots, curling patterns, and getting a ranked list of possible causes with suggested tests to narrow it down. Not "it might be this" but "test for this first, and if that's negative, then check for this."
- **Species interaction.** Understanding which plants compete for the same nutrients, which fix nitrogen and help their neighbors, which attract beneficial insects that protect others. The garden as a *system*, not a collection of individuals.
- **Seasonal planning.** When to prune, when to fertilize, when to leave things alone — calibrated to my specific climate and microclimate conditions.

This is AI as *consultant*. I observe, I describe, I ask questions. The AI draws on broad botanical knowledge and applies it to my specific situation. It works surprisingly well.

But it has a fundamental limitation.

---

## The Gap

Claude cannot *see* my garden.

Every diagnosis depends on my descriptions — how accurately I describe a leaf color, how precisely I estimate sun exposure, how reliably I notice the early signs of a problem. I am the sensor, and I am a noisy, intermittent, biased sensor. I notice the dramatic (a whole branch dying) and miss the subtle (a slight yellowing at the leaf margins that, three weeks from now, will indicate an iron deficiency).

There's an information bottleneck: the AI has vast botanical knowledge but zero direct access to the actual physical state of the garden. It's like having a brilliant doctor who can only diagnose patients over the phone, based on the patient's own description of their symptoms.

This works. But it could work so much better.

---

## AI as Observer

![A tiny insect-like micro-drone scanning a plant leaf with a gentle blue light](/assets/images/ai-garden/micro-drone.jpg)

My kids and I have been imagining the next step.

What if the AI could *see*? Not through my descriptions, but directly — through cameras, sensors, and small autonomous agents in the garden?

**Level 1: Passive monitoring.** Soil sensors at multiple points measuring pH, moisture, temperature, and mineral content continuously. Small cameras capturing daily snapshots of each plant. An AI that watches the garden the way a time-lapse camera watches a construction site — noticing changes that happen too slowly for human perception. That slight yellowing at the leaf margins? The AI catches it on day one, not day twenty-one.

**Level 2: Active inspection.** This is where the kids' imagination goes. Micro-drones — small as hummingbirds, gentle as butterflies — that can fly to a specific plant and inspect it up close. Zoom in on a leaf surface to check for mites. Examine the underside of a branch for scale insects. Hover near the soil to look for signs of fungal growth at the root crown. Not on a schedule, but on *suspicion* — the AI notices something in the sensor data that doesn't look right, and dispatches a drone to go look closer.

The key phrase is **"based on an AI's doubt."** The AI has a model of how the garden should look. When reality deviates from the model, the AI gets curious. It sends a drone to investigate. This is *exactly* the kind of autonomous epistemic behavior I explore in the [PKT open questions](../popper/questions) — an AI that forms hypotheses, notices when observations don't match, and takes action to resolve the uncertainty.

**Level 3: Diagnostics.** A drone that doesn't just look, but tests. Takes a tiny leaf sample and runs it through an onboard spectrometer. Tests soil from a suspicious patch. Identifies whether a discoloration is nutrient deficiency, fungal infection, or viral disease — with the kind of precision that currently requires sending samples to a lab and waiting two weeks.

---

## AI as Actor

And then the step that feels both exciting and unsettling: AI that *intervenes*.

A drone that identifies an aphid colony and deploys a targeted biological control — releasing ladybugs precisely where they're needed, or applying a microscopic dose of neem oil to just the affected branch. Not blanket spraying the whole garden, but precision intervention based on diagnosis.

An AI that detects a viral infection in one branch and makes a recommendation: **amputate** this section before it spreads, or **graft** a resistant variety onto the existing rootstock. Not performing the surgery itself (not yet), but identifying the problem, proposing the solution, and perhaps preparing the site.

An AI that notices that one section of the garden consistently underperforms and suggests a *redesign* — "these three species are competing for the same nutrients in this soil type; if you move the frangipani to the upper terrace and replace it with a nitrogen-fixing ground cover, both sections will benefit."

This is AI moving from *knowing about* gardens to *participating in* gardens. From consultant to collaborator.

---

## The Physical World Is Different

Everything I've described in the sections above is technically within reach — soil sensors exist, micro-drones exist, computer vision for plant health is an active research area. But there's something fundamentally different about AI in the physical world that's worth pausing on.

Digital AI operates in a clean, deterministic environment. Text goes in, text comes out. The same input produces the same output. Errors are correctable — regenerate the response, try again.

A garden doesn't work like that.

Soil has memory. A pH imbalance you don't catch in March becomes a dead plant in July. A pest colony you miss today is an infestation next week. The physical world has **irreversibility** — you can't regenerate a dead tree. You can't undo a missed diagnosis.

Weather is unpredictable. A hailstorm doesn't care about your AI's model. A sudden frost doesn't consult the seasonal planning algorithm. The physical world has **chaos** — small perturbations lead to large, unpredictable consequences.

And living things are not passive objects. A plant responds to your interventions. Prune it and it redirects growth. Fertilize it and it shifts resource allocation. The garden is a **feedback system** — the AI's actions change the system the AI is trying to model.

This is what makes AI in the physical world harder, and more interesting, than AI in the digital world. It requires something closer to real intelligence: the ability to deal with uncertainty, irreversibility, feedback, and systems that have their own agenda.

---

## What I'm Learning

Gardening with AI has taught me something about both gardening and AI:

**About gardening:** The plants were always trying to tell me things. The leaf color, the growth direction, the flowering pattern — these are all signals. I just didn't have the knowledge to read them reliably. AI fills the translation gap: it turns my observations into diagnoses, and my diagnoses into actions. The garden hasn't changed. My ability to listen to it has.

**About AI:** AI is remarkably good at *reasoning from descriptions* but it has no ground truth of its own. Everything it knows about my garden comes through me. The biggest unlock won't be smarter models — it will be giving AI *eyes and hands*. Direct access to the physical world changes what AI can do more than any amount of parameter scaling.

**About the future:** My kids see this instinctively. They don't draw a line between "digital" and "physical" the way my generation does. To them, a micro-drone checking a plant for pests is as natural as using a phone to look something up. The future of AI isn't just better chatbots. It's AI that touches the world — soil, water, leaves, roots.

I'm going to keep exploring this. The garden journal below documents the specifics — plant by plant, problem by problem, season by season.

---

## Garden Journal

Each of these pages tells the story of a specific plant in the garden — what went wrong, what AI diagnosed, what worked, and what I learned. They're grounded in real conversations, real treatments, and real results.

| Plant | Story | Status |
|-------|-------|--------|
| [Bougainvillea](bougainvillea/) | The stress lover — less water, more flowers | Sparkling pink and white |
| [Night Jasmine](night-jasmine/) | From quiet wallflower to explosive growth | Going bonkers |
| [Hibiscus](hibiscus/) | The virus detective story — differential diagnosis | 9 blooming, 1 under investigation |
| [Plumeria](plumeria/) | Clusters on every stem — finding the right formula | Dense flowering |
| [Roses](roses/) | Larger and brighter — and learning to wait | Between flushes |

*More species pages coming as the garden grows and the stories develop.*

---

*This is a living essay. Updated as the garden grows and the AI gets better at helping it.*
