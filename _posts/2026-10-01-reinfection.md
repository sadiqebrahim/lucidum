---
date: 2026-10-01 11:05:00 +0530
title: Reinfections travel like a wave
dek: A new disease model counts how many times each person has been infected, and finds the whole population climbing that ladder together, like a wave with a speed you can calculate.
topic: Health
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-01-reinfection/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Life-time patterns of reinfections: epidemic cohorts as traveling waves, P. Castioni, C. Poletto and A. Arenas, arXiv 2609.33466 (27 Sep 2026)"
    url: https://arxiv.org/abs/2609.33466
    note: (preprint)
---

Your fifth cold isn't like your first. Your immune system has seen it before. Yet most models of how diseases spread treat every infection the same. A [new model](https://arxiv.org/abs/2609.33466) keeps count, and finds a pattern hiding in a lifetime of infections.

## The usual shortcut

Models that allow reinfection, such as the classic SIS and SIRS frameworks, put people into boxes like "susceptible", "infected" and "recovered". Someone who recovers can later fall ill again. But every infection counts the same and is treated as independent, so the model forgets each person's history.

## A ladder of infections

Piergiorgio Castioni, Chiara Poletto and Alex Arenas propose a minimal "chain SIR" model. Instead of one set of boxes, there is a set for each infection count: first infection, second, third and so on. Each step up is a rung on a ladder.

The rates can change with each rung: how easily you catch the disease, how quickly you recover and how fast your protection wanes. As immunity builds, the climb can slow.

## The whole population moves like a wave

The surprise is in the overall behaviour. The dynamics produce a steady flow up the ladder, and the population moves as a <mark>travelling wave in reinfection space</mark>: a bulge of people at one rung, then the next, then the next.

![A curve of the share of people against the number of past infections, peaking and moving to the right over time.]({{ '/assets/posts/2026-10-01-reinfection/wave.png' | relative_url }})
*The population's infection count moves up the ladder like a wave (schematic).*

The team derived an analytical formula for the wave's speed and set out the general conditions under which such cohort waves appear and persist. They suggest this offers a new way to read long-term prevalence patterns, including endemic disease that is structured by age or immunity.

## Checked against real data

They then compared the speed formula with longitudinal cohort data, studies that follow the same people for years. From that comparison they estimated how much immune responses reduce the reinfection rate for several seasonal viruses, including influenza A/H3N2 and respiratory syncytial virus (RSV).

## The catch

This is a preprint and hasn't been peer reviewed. The model is deliberately minimal, and the immunity estimates depend on how well the cohort data match its assumptions. The abstract doesn't give the size of the reductions, so we don't quote numbers here.
{: .catch}

Reinfections follow a lifetime pattern, and now there's a way to measure it.
