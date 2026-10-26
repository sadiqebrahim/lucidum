---
date: 2026-10-15 22:55:00 +0530
title: Could balanced AI summaries make the news more polarised?
dek: A game-theory model finds that once AI news summaries get reliable enough, outlets lose their least loyal readers and lean harder into the slant their remaining fans want.
topic: Economics
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-15-ai-summaries/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "AI Information Synthesis and Content Polarization, Chang Liu and Yuting Zhu, arXiv 2610.17674 (13 Oct 2026)"
    url: https://arxiv.org/abs/2610.17674
    note: (preprint)
---

If an AI can give you a fair, balanced summary of all the news, you'd expect the news to get calmer. A [new economics paper](https://arxiv.org/abs/2610.17674) argues it can work the other way, not because of the AI itself but because of how news outlets respond to it.

## The model

Chang Liu and Yuting Zhu build a game-theory model. Readers gather information to make decisions. Content producers, think news outlets, have limited capacity, and split it between two kinds of information: "vertical" information that's broadly useful to everyone, and "horizontally differentiated" content tailored to their own audience's tastes, which we'll call slant. Then the model adds an AI that synthesises balanced information as an alternative source.

## Three phases

What happens depends on how reliable the AI is:

- **Low reliability:** the AI has no effect on the market.
- **Middling reliability:** the AI disciplines prices, since outlets can't charge as much, but readers don't switch and content doesn't change.
- **High reliability:** readers start substituting towards the AI, and outlets respond by moving capacity away from shared facts and <mark>towards differentiated content</mark>, increasing polarisation.

![A curve of polarisation against AI reliability, flat at first and then rising; it rises less steeply when there are many outlets.]({{ '/assets/posts/2026-10-15-ai-summaries/polarisation.png' | relative_url }})
*In the model, polarisation rises once the AI is reliable enough, and less so with more competing outlets (schematic).*

## Why the slant grows

The mechanism runs through who leaves. The readers the AI attracts are the ones least well matched to any particular outlet. The loyal audience stays. Left with readers who most want their particular angle, outlets have stronger reasons to cater to them.

The polarisation effect strengthens as the AI becomes more reliable and weakens when more outlets compete with each other.

## A wedge between direct and overall effects

The authors' broader point is that a technology's direct effect and its equilibrium effect can point in opposite directions. Each reader who uses the AI gets more balanced information. The wider content ecosystem, after everyone adjusts, can end up more polarised.

## The catch

This is a theoretical model and a preprint, not yet peer reviewed. It shows that this outcome is possible under its assumptions, not that it is happening. There is no empirical test in the paper's abstract.
{: .catch}

A balanced tool doesn't guarantee a balanced world, because everyone else reacts to it.
