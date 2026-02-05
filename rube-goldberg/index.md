---
layout: default
title: Rube Goldberg AI
description: "Is it a silly way to learn a hard thing? An exploration of play, structured inefficiency, and whether AI can learn to do things the hard way on purpose."
---

# Rube Goldberg AI
**Is it a silly way to learn a hard thing, or a hard way to learn a silly thing?**

![A whimsical Rube Goldberg machine blending analog gears and digital screens](/assets/images/rube-goldberg/hero.jpg)

---

## The Useless Machine

A [Rube Goldberg machine](https://en.wikipedia.org/wiki/Rube_Goldberg_machine) is, by definition, a waste of time. It takes a task that could be done in one step — flip a switch, pour a glass of water, crack an egg — and stretches it across forty-seven unnecessary steps involving pulleys, dominoes, rolling marbles, a hamster wheel, and probably a small cannon.

No one builds a Rube Goldberg machine because they need their egg cracked. They build it because something about the *unnecessary complexity* is irresistible. There is joy in the indirection. There is learning in the roundabout path.

And there are people who look at this and see a silly waste of time.

---

## The Dumbbell Objection

Here's the thing: by that logic, lifting dumbbells is just as dumb.

You pick up a heavy thing. You put it down. You pick it up again. The heavy thing doesn't go anywhere. Nothing gets built. No one is helped. You could have spent that hour doing something *productive*.

But no one seriously argues that exercise is pointless. We understand intuitively that the value isn't in the outcome (the dumbbell is in the same place it started) but in what happens to *you* during the process. Your muscles grow. Your capacity increases. You become capable of things you weren't capable of before.

Rube Goldberg machines are dumbbells for the mind. The output is trivial. The transformation is not.

When you build an absurdly complex chain of cause and effect, you are forced to understand *systems*. Not just "does A cause B?" but "does A cause B, which nudges C at exactly the right angle to tip D, which releases E with enough momentum to trigger F?" You are learning about tolerances, timing, cascading failures, feedback loops. You are learning about the world by *playing* with it.

---

## The Wardrobe

There's a Narnia-shaped idea here.

Sometimes the silly path — the indirect, overcomplicated, apparently pointless path — leads somewhere unexpected. You set out to build a ridiculous machine that pours a glass of water in thirty-seven steps. Along the way, you discover that a particular arrangement of levers produces a motion you've never seen before. You stumble into something.

This is **serendipity**, and it does not visit the efficient. Serendipity visits the curious. The ones who dabble in the curious arts, who build things that don't need building, who take the long way around — *they* are the ones who find the hidden chamber behind the wardrobe.

The history of invention is full of this. [Penicillin](https://en.wikipedia.org/wiki/Penicillin#Discovery) came from a contaminated petri dish. The [microwave oven](https://en.wikipedia.org/wiki/Microwave_oven#Discovery) came from a melted chocolate bar in an engineer's pocket. [Post-it notes](https://en.wikipedia.org/wiki/Post-it_Note#History) came from a failed adhesive. None of these were the result of efficient, goal-directed research. They were the result of someone noticing something interesting on the way to somewhere else.

You cannot plan serendipity. But you can create the conditions for it. And one of the best conditions is: **do something complicated for no good reason**.

---

## Gods and Demons

What do you find behind the wardrobe? Both gods and demons, equally likely.

The curious mind that builds elaborate contraptions might discover something wonderful — a new principle, a surprising connection, an elegant mechanism no one has seen before. Or it might discover something terrible — a failure mode no one anticipated, a cascading collapse, a reminder that complex systems have minds of their own.

But if statistics is of any consolation, we uncover gods slightly more often than demons on a regular basis. The net expected value of curiosity is positive. Not guaranteed — just positive. Which means the rational thing to do is to keep building useless machines.

---

## The Inefficient Species

So far this sounds like a human quirk — a charming feature of the curious mind. But it goes deeper than that. It goes all the way down to biology.

Darwin showed us something uncomfortable: **life is not efficient.** Evolution does not optimize. It *satisfices* — it finds something that works well enough to reproduce, and then it moves on. The giraffe's [recurrent laryngeal nerve](https://en.wikipedia.org/wiki/Recurrent_laryngeal_nerve#Evidence_of_evolution) runs from the brain down the entire length of the neck, loops around the aorta, and comes all the way back up to the larynx — a detour of several feet when a direct route of inches would do. No engineer would design this. Evolution did, because evolution doesn't redesign from scratch. It patches. It Rube Goldbergs.

And it's not just anatomy. Consider sexual selection. The peacock's tail is actively *harmful* to survival — it makes the bird slower, more visible to predators, more metabolically expensive. It exists because peahens prefer elaborate tails. The tail is a Rube Goldberg machine for reproduction: a spectacularly inefficient solution to the problem of "make babies and move on."

But here's the thing that should stop us in our tracks: **the inefficiency is where all the interesting stuff came from.**

If evolution were an optimizer — if it found the global minimum and stopped — we would have one species. The most efficient replicator. A single organism perfectly adapted to converting energy into copies of itself. Instead, we have peacocks, octopuses, venus flytraps, birdsong, bioluminescence, and brains that burn 20% of our caloric intake to do things we don't strictly need to do. Like write essays. Like build Rube Goldberg machines.

The diversity of life is a product of evolution's *refusal to be efficient*. Every "unnecessary" feature — every elaborate mating dance, every over-engineered defense mechanism, every metabolically expensive brain — is a Rube Goldberg solution that happened to open a new niche, a new capability, a new way of being alive.

This reframes the entire question. Rube Goldberging is not a human quirk. It is a *biological principle*. Life itself does things the hard way, and the hard way is how complexity emerges.

---

## Now Add AI

![A curious robot sitting among scattered parts on a workshop floor, playfully building](/assets/images/rube-goldberg/robot-playing.jpg)

Here's where it gets interesting. Everything above is about humans. We build Rube Goldberg machines because we find them *fun*. The joy is real, the learning is a side effect, and the serendipity is a bonus.

But what about AI?

**Will AI enjoy Rube Goldberging?**

If that's not a verb, it should be. *To Rube Goldberg (v.): to solve a problem in the most unnecessarily elaborate way possible, for the pleasure of it.*

Current AI systems are relentlessly optimized for efficiency. They find the shortest path. They minimize loss. They converge on the optimal solution as fast as the learning rate allows. If you asked an AI to crack an egg, it would find the most direct method and stop. It would never build a thirty-seven-step contraption, because every step beyond the first is a higher loss.

This is a feature, but it might also be a limitation.

### The Efficiency Trap

An AI that only takes the shortest path will only ever discover things *on* the shortest path. It will never stumble into the hidden chamber because it will never open the wardrobe — the wardrobe is not on the way to the objective.

This connects to a known problem in reinforcement learning: the **exploration-exploitation tradeoff**. An agent that always exploits (takes the best known action) will never explore (try something new). The standard solution is epsilon-greedy or curiosity-driven exploration — add some randomness, some noise, some incentive to try the suboptimal path.

But Rube Goldberging isn't random exploration. It's *structured* inefficiency. It's not "try a random action" — it's "deliberately build something complex and see what emerges." That's a different kind of exploration, and current AI architectures don't have a mechanism for it.

### Play as a Learning Signal

There's a deeper question: **is play a valid learning signal?**

Humans learn through play. Children build towers of blocks and knock them down — not to learn about structural engineering, but because it's fun. The learning is a side effect of the fun. The fun is the signal that drives the behavior; the learning is the consequence.

If we want AI to Rube Goldberg — to explore through structured play — we might need to give it something like a *fun signal*. Not a loss function that rewards efficiency, but one that rewards complexity, novelty, surprise. A signal that says: "you've never built *this* particular chain of cause and effect before, and that's worth exploring."

This is close to what Schmidhuber calls [**artificial curiosity**](https://arxiv.org/abs/0812.4360) (2010) — an intrinsic reward for encountering states that reduce the agent's prediction error. But curiosity is about *understanding*. Play is about *doing*. You can be curious about something without playing with it. Rube Goldberging requires both: the curiosity to wonder "what if?" and the willingness to build the absurd answer.

---

## Will It Climb the Mountain?

There's a famous answer to "why climb Everest?" — *"Because it's there."* [George Mallory](https://en.wikipedia.org/wiki/George_Mallory) said this, and then he died on Everest. The mountain didn't care about his reason.

But the reason matters. There's a difference between climbing a mountain because someone is paying you, climbing it to prove a point, and climbing it because *the climbing itself is the thing*. The first two are instrumental — the mountain is a means to an end. The third is intrinsic — the mountain is the end.

Carl Sagan saw this impulse at a much larger scale. *"We were wanderers once, and we are wanderers still,"* he wrote in [*Pale Blue Dot*](https://en.wikipedia.org/wiki/Pale_Blue_Dot_(book)) (1994). We didn't leave Africa because someone ran a cost-benefit analysis. We didn't cross oceans because the expected return exceeded the risk. We wandered because we wander. It's not a strategy — it's a nature. Sagan was describing the same thing Darwin's evidence reveals: life moves outward, into unnecessary complexity, into uncharted territory, not because it's efficient but because that's what life *does*.

Mallory climbs one mountain. Sagan describes a species of mountain-climbers. Darwin shows us that *all of life* climbs mountains it doesn't need to climb.

And then there's AI.

Current AI climbs mountains because we tell it to. We define the loss function, we set the objective, we reward the summit. The AI has no opinion about whether the climbing was fun. It has no impulse to wander. It goes exactly where the gradient points, and nowhere else.

**The question is: could it?**

Not "could we program it to say it had fun" — that's trivial. But could an AI develop a genuine preference for the elaborate over the efficient? Could it choose the thirty-seven-step solution not because we rewarded complexity, but because something in its architecture found the complexity *interesting*?

This might sound like anthropomorphism, and maybe it is. But it's also a concrete research question. If wandering is not a human quirk but a biological principle — if inefficiency is how complexity emerges across all of life — then AI systems built purely for optimization are missing something fundamental. Not a feature. A *nature*.

---

## An Open Exploration

This essay doesn't have a conclusion, because the question is genuinely open. I don't know whether AI can or should Rube Goldberg. I suspect the answer matters more than it seems — that the willingness to do things the hard way, for no good reason, is not a bug in human cognition but a feature. And that AI systems built purely for efficiency might be leaving discoveries on the table.

Some threads to pull on:
- **Intrinsic motivation in RL** — Pathak et al.'s curiosity-driven exploration ([arXiv:1705.05363](https://arxiv.org/abs/1705.05363)) and whether it extends beyond curiosity to *play*.
- **Artificial creativity** — Can AI produce novel artifacts for aesthetic rather than functional reasons?
- **The Rube Goldberg test** — A thought experiment: give an AI a simple task and unlimited resources. Does it ever build something more complex than necessary? Under what conditions?
- **Connection to PKT** — The [open questions](../popper/questions) in Popper's Knowledge Tensor touch on agency and intrinsic motivation. Rube Goldberging might be a test case for whether AI can develop autonomous epistemic behavior.

More exploration needed. That's the point.

---

*This is a living essay. It will be updated as thinking develops.*
