---
layout: default
title: "All Security Is Theater"
description: "Security is a feeling, not a state — and AI is about to stress-test both sides. An exploration of what happens when the tools of offense and defense become symmetric."
---

# All Security Is Theater
**On locks, gas cutters, and the coming AI arms race in cybersecurity**

![A glowing digital lock being simultaneously reinforced and dismantled by opposing streams of light](/assets/images/ai-security/hero.jpg)

---

## The Feeling of Security

A lock on a door creates a feeling. You turn the bolt, hear the click, and something in your brain registers *safe*. But the lock hasn't changed what's physically possible — it's changed what's *convenient*. A determined person with the right tools can still get through. A lock is a filter for effort, not an absolute barrier.

This is the foundational truth about security that we prefer not to think about: **all security is a feeling of being secure, until it isn't.**

The lock is safe until someone invents a gas cutter. The encryption is safe until someone builds a faster computer. The deception is safe until someone becomes aware of the deception. Security doesn't exist as a fixed state — it exists as a temporary gap between what the defender has built and what the attacker hasn't yet figured out.

And now we're handing both sides the most powerful pattern-recognition and problem-solving tool ever created.

---

## Security Through Obscurity

A surprising amount of our digital security rests on a single foundation: **someone else's inability to guess.**

Your bank account is protected because no one can guess your password (hopefully). Your encrypted messages are safe because no one can factor the large primes that generated your keys — not in any reasonable amount of time, not with any existing hardware. Your identity is secure because no one has assembled enough of your scattered personal data to impersonate you convincingly.

This is security through obscurity at every level:

- **Passwords** — the attacker can't guess your string
- **Encryption** — the attacker can't reverse-engineer your key
- **Authentication** — the attacker can't replicate your identity signals
- **Network security** — the attacker can't find the vulnerability in your code
- **Social engineering** — the attacker can't craft a convincing enough lie

Every one of these depends on asymmetric capability — the defender knows something the attacker doesn't, or the defender can do something the attacker can't. Security is the *gap* between the two sides.

AI closes gaps. That's what it does.

---

## The Symmetric Arms Race

Here's what makes AI in security different from previous technological shifts. A gas cutter changes the equation for locks but doesn't help you build better locks. A faster computer breaks old encryption but also enables new encryption. The tools have historically been asymmetric — good for one side, maybe useful for the other.

AI is symmetric. The same tool, the same capability, works for both attack and defense:

**Offense:**

`AI → reconnaissance → find vulnerabilities → craft exploits → infiltrate → exfiltrate`

An AI system can scan codebases for vulnerabilities faster than any human team. It can generate phishing emails that are indistinguishable from genuine communication. It can adapt its attacks in real-time based on the defender's responses. It can try millions of approaches in the time a human tries one.

**Defense:**

`AI → monitor → detect anomalies → patch vulnerabilities → respond → harden`

The same AI capabilities can monitor network traffic for suspicious patterns, detect zero-day exploits by recognizing anomalous behavior, generate patches faster than humans can review code, and respond to breaches in milliseconds rather than hours.

Same technology. Same capabilities. Deployed on opposite sides of the wall.

This is the scenario that keeps security professionals awake at night — not that AI makes attacks possible (attacks were always possible) but that AI makes the arms race move at machine speed instead of human speed.

---

## The New Exploits

Here's where it gets genuinely unsettling.

Every known vulnerability class — SQL injection, buffer overflow, cross-site scripting, privilege escalation — was discovered by a human who noticed a pattern, a gap, an unintended behavior. These discoveries took time, insight, and creativity.

AI doesn't need insight the way humans do. It needs data and compute. Given enough of both, it can explore the space of possible vulnerabilities with a thoroughness that no human team could match.

What this means in practice:

**AI finding known classes faster.** Every piece of software has bugs. AI-powered scanning tools can find them orders of magnitude faster than manual code review. This is already happening — and it benefits defense as much as offense. The question is who finds them first.

**AI discovering new classes.** This is the frontier that matters. Human security researchers discover new vulnerability classes every few years — it's a slow, creative process. AI might compress this timeline dramatically. A model trained on the history of vulnerabilities could potentially recognize *patterns of vulnerability patterns* — meta-vulnerabilities that humans haven't conceptualized yet.

**AI crafting novel attacks.** Not just finding the hole, but designing the optimal way through it. AI can generate social engineering attacks customized to individual targets. It can craft exploits that adapt to the specific configuration of the target system. It can chain together multiple small vulnerabilities into a compound attack that no individual vulnerability would enable.

And somewhere, in a classified lab or a criminal operation or a nation-state cyber unit, someone has probably already done this. The zero-day vulnerabilities we know about are the ones that have been disclosed. The ones we don't know about are the ones that matter.

---

## The Good Guy With a Gun

There's an uncomfortable American saying: *the only thing that stops a bad guy with a gun is a good guy with a gun.* Whatever you think of it in the physical world, it's disturbingly accurate in cyberspace.

In the digital world, the weapons are available to everyone. Open-source security tools, penetration testing frameworks, AI models — they don't check your intentions before responding. Kali Linux doesn't ask if you're a security researcher or a criminal. Claude doesn't know if you're hardening your own systems or probing someone else's.

The tools are symmetric, the access is symmetric, and increasingly the skill required is dropping toward zero. You used to need deep technical expertise to find and exploit a vulnerability. AI is democratizing that capability — for both sides.

This creates a world where:

- **Defensive AI is not optional.** If attackers are using AI, defending without AI is bringing a knife to a gunfight. Every organization needs AI-powered security monitoring, not as a luxury but as a baseline.
- **Speed becomes the differentiator.** When both sides have comparable tools, the advantage goes to whoever moves faster. AI-powered defense that detects and responds in seconds beats AI-powered offense that needs minutes to establish a foothold.
- **The detection game changes.** Traditional security monitors for known signatures — patterns that match previous attacks. AI-powered attacks will generate novel signatures every time. Defense needs to shift from pattern-matching to anomaly detection — not "does this look like a known attack?" but "does this behavior look normal?"

---

## Software Is Especially Fragile

Software security deserves special attention because it sits at the uncomfortable intersection of complexity and importance.

The entire digital economy runs on code that was written by humans under deadline pressure, reviewed incompletely, tested against known scenarios, and deployed with fingers crossed. Every web application, every API, every database connection is a potential entry point. The attack surface is enormous and growing.

Most of our sense of digital security comes from a simple fact: **there are more systems to attack than there are attackers to attack them.** Security through obscurity at scale — your small company probably won't be targeted because there are bigger targets. Your personal accounts probably won't be compromised because there are easier victims.

AI removes the scale constraint. An AI-powered attack doesn't need to choose targets — it can probe all of them, simultaneously, continuously. The protection of being small, obscure, or uninteresting evaporates when the attacker's cost per target approaches zero.

And software is getting *easier* to write — which means more software, written faster, with more potential vulnerabilities, deployed by people with less security expertise. AI-assisted coding is a productivity revolution, but every line of code is also a potential attack surface.

---

## Evolving Security

So where does this leave us?

Not in despair, but in a new posture. Security has always been an arms race — lock, better lock pick, better lock, better lock pick. AI accelerates the cycle but doesn't change its nature. What changes is the speed and the stakes.

**Security becomes continuous, not periodic.** Annual penetration tests become real-time AI monitoring. Security audits become automated scanning pipelines. The wall isn't built once — it's rebuilt constantly.

**Security becomes adversarial by design.** The best way to test a defense is to attack it — with your own AI. Red team / blue team exercises become AI vs AI simulations. You find your vulnerabilities before someone else does. The same tools that enable attack enable testing.

**Security becomes probabilistic, not binary.** We stop asking "is this system secure?" (the answer is always "no, not absolutely") and start asking "how quickly can we detect and respond to a breach?" Assume compromise. Design for resilience. The question isn't whether the wall will be breached — it's how fast you can rebuild it.

**Security becomes a conversation between AIs.** On one side, AI probing for weaknesses. On the other, AI watching for probes. Between them, an escalating dialogue conducted at machine speed, with humans setting policy but no longer driving the moment-to-moment decisions. We become the generals, not the soldiers.

---

## The Uncomfortable Conclusion

All security has always been theater — a performance that creates a feeling of safety while both sides know, at some level, that it's temporary. The lock deters the casual intruder. The firewall blocks the script kiddie. The encryption holds until the next mathematical breakthrough.

AI doesn't change this fundamental truth. It accelerates it. The cycles get shorter. The exploits get more sophisticated. The defenses get more automated. And the feeling of security becomes harder to maintain because the evidence of its fragility becomes more visible.

The question isn't whether AI will transform cybersecurity — it already is. The question is whether we're honest enough to stop pretending that any system is "secure" and start building for the world as it actually is: a world where security is a process, not a product, and where the tools of creation and destruction are the same tools, held by different hands.

---

*An exploratory essay. Updated as the AI security landscape evolves.*
