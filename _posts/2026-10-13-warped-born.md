---
date: 2026-10-13 23:52:00 +0530
title: Change one number in quantum physics, and looking freezes a gas
dek: A thought experiment warps quantum theory's Born rule from a square to a power of 2b, and finds that repeatedly watching a gas makes it clump and freeze, like Maxwell's demon.
topic: Physics
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-13-warped-born/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "A Warped Born Rule Turns an Observer into a Maxwell's Demon, Olumakinde Ogunnaike, arXiv 2610.13936 (9 Oct 2026)"
    url: https://arxiv.org/abs/2610.13936
    note: (preprint)
---

Quantum mechanics is famously delicate: change almost any part of it and the predictions go haywire. A [new paper](https://arxiv.org/abs/2610.13936) by physicist Olumakinde Ogunnaike tests one of its most basic rules, and finds that a small change would turn the simple act of looking into something like Maxwell's demon.

## The rule being changed

In quantum theory a system is described by a wavefunction ψ. The Born rule says how that turns into the probabilities we see: the chance of a measurement outcome m is the squared size of the matching part of the wave,

p(m) ∝ ‖P_m ψ‖².

That exponent 2 is what links the abstract wave to the statistics of experiments.

Ogunnaike asks what happens if the rule is warped to

p_b(m) ∝ ‖P_m ψ‖^(2b),

so that ordinary quantum mechanics is b = 1.

## Watching a gas

The paper looks at systems where the number of particles is conserved, such as a gas of particles in a row, which evolve between repeated local measurements of where the particles are. With the warped rule, some measurement histories become more likely than they should be, and the direction of that bias depends on whether b is above or below 1.

- **b > 1:** the gas tends to collect into <mark>nearly frozen configurations</mark>, clumps that stop moving. Observation alone seems to pull entropy out of a closed system, much like Maxwell's demon, the imaginary creature that sorts molecules to reduce disorder.
- **b < 1:** the bias reverses. Long-wavelength fluctuations get scoured out and the gas becomes hyperuniform, spread out more evenly than a random gas would be.

![Two rows of particles under repeated observation: for b greater than one they clump together; for b less than one they spread out evenly.]({{ '/assets/posts/2026-10-13-warped-born/demon.png' | relative_url }})
*Under a warped Born rule, watching makes a gas clump (b > 1) or spread unusually evenly (b < 1). Schematic.*

Both phases are derived analytically for a one-dimensional quantum gas under a particular measurement scheme. They are then checked numerically for more general measurement circuits using matrix-product-state simulations.

## Why it matters

There are two reasons. First, it's another demonstration of how rigid quantum theory is. Nudge the Born rule even slightly and you get wildly unphysical behaviour, such as an observer that lowers entropy just by looking. That is a kind of argument for why the rule is what it is.

Second, the warped rule isn't purely hypothetical as a calculation tool. The "replica trick", a widely used technique in physics, effectively works with powers like this. The paper argues the bias shows up there too, implying qualitative differences between calculations done at a finite number of replicas and those taken to the replica limit.

## The catch

This is a thought experiment about a hypothetical rule. Nothing in the paper suggests nature actually departs from the Born rule. The analytic results cover one measurement scheme in one dimension, and the broader claims rest on simulations. It's also a preprint that hasn't been peer reviewed.
{: .catch}

Square the wave and the world behaves. Change the square, and even looking starts to change things.
