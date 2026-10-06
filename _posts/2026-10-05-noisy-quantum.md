---
date: 2026-10-05 23:52:00 +0530
title: Your laptop can fake a noisy quantum computer
dek: A new proof shows that once noise builds up locally, an ordinary computer can sample the output of noisy quantum circuits efficiently, at a depth that doesn't grow with the size of the chip.
topic: Quantum computing
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-05-noisy-quantum/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "A polynomial-time classical sampler for noisy quantum circuits from statistical mechanics, Nelson, Rajakumar, Yin, Zhang et al., arXiv 2610.00548 (30 Sep 2026)"
    url: https://arxiv.org/abs/2610.00548
    note: (preprint)
---

Quantum computers are supposed to do things no ordinary computer can. But today's chips are noisy, and a [new proof](https://arxiv.org/abs/2610.00548) shows that <mark>once that noise builds up, an ordinary computer can copy them</mark>, at least for a broad class of circuits.

## A little noise, every step

In real hardware, every qubit has a small chance p of being scrambled at each step. Noise slowly erases the quantum information that makes these machines hard to simulate. The question is how quickly.

## The old view: bigger chips are safer

Earlier classical sampling methods needed the circuit to be deep enough for noise to push the whole chip's output close to a trivial state, and that depth grew with the logarithm of the number of qubits. That suggested bigger chips would stay out of reach for longer.

## The new result: a fixed depth is enough

The authors prove that local build-up of noise is already sufficient. For geometrically local circuits (qubits interact only with their neighbours) made of unital operations with single-qubit depolarizing noise of strength p, once the depth exceeds about (1/p)·log(1/p), a classical computer can approximately sample the output in polynomial time. That depth depends on the noise, not on the size of the chip.

![Depth needed against chip size: the old requirement grows with size, the new one is flat, set by the noise level.]({{ '/assets/posts/2026-10-05-noisy-quantum/depth.png' | relative_url }})
*Depth ≳ (1/p)·log(1/p), independent of chip size (curves schematic).*

The proof borrows from statistical mechanics: the circuit's output is mapped to a "polymer model", and a convergent cluster expansion, combined with a property of depolarizing noise called hypercontractivity, shows it can be computed efficiently.

![A grid of qubits with clusters outlined, standing for the polymer model used in the proof.]({{ '/assets/posts/2026-10-05-noisy-quantum/polymer.png' | relative_url }})
*The polymer picture (schematic).*

## Why it matters

Claims of quantum advantage on noisy hardware have to beat the best classical simulations. This result draws a clearer line: deep, noisy, local circuits without error correction can be simulated, so advantage has to come from shallow circuits or from error-corrected machines.

The result applies to geometrically local circuits with this kind of noise; it says nothing about error-corrected quantum computers, and "polynomial time" can still mean a lot of computing in practice. It's a preprint and hasn't been peer-reviewed.
{: .catch}

Without error correction, deep noisy quantum circuits lose their edge.
