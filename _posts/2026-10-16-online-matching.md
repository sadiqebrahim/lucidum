---
date: 2026-10-16 23:21:00 +0530
title: The best any ride app can do is match 82%
dek: Mathematicians have found a strategy that reaches the proven ceiling for matching people as they arrive, 1 − e/e^e or about 82% of what hindsight would achieve.
topic: Mathematics
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-16-online-matching/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Optimal Online Stochastic Matching, Paul Dütting, Michal Feldman and Mathieu Molina, arXiv 2610.19866 (14 Oct 2026)"
    url: https://arxiv.org/abs/2610.19866
    note: (preprint)
---

Open a ride app and requests appear one at a time. Each has to be matched to a driver on the spot, before anyone knows who will ask next. A [new paper](https://arxiv.org/abs/2610.19866) settles exactly how well any such on-the-spot strategy can ever do: about <mark>82% of the hindsight optimum</mark>.

## Matching without seeing the future

The problem is called online matching. Demands arrive over time, each must be paired immediately and irrevocably, and you're scored against the best matching you could have made with hindsight, knowing every arrival in advance. Ride apps are our illustration; the same structure appears in delivery, ad slots and any marketplace that pairs people as they show up.

This paper studies the unweighted version, where every successful match counts the same, with a known arrival law: you don't know who's coming next, but you do know the statistics of how arrivals happen.

## The ceiling

An earlier paper (Chierichetti, Giacchini, Panconesi and Vattani, ICALP 2025) proved that no online strategy can beat a competitive ratio of

1 − e/eᵉ ≈ 0.8206

for Poisson arrivals. That is the ceiling. What was missing was a strategy that actually reaches it.

![The formula 1 minus e over e to the e, approximately 0.82, above a bar filled to 82% of the hindsight score.]({{ '/assets/posts/2026-10-16-online-matching/ceiling.png' | relative_url }})
*No on-the-spot strategy can beat about 82% of hindsight. The new paper shows one that gets there.*

## Reaching it

Paul Dütting, Michal Feldman and Mathieu Molina close the gap. For Poisson arrivals their method achieves exactly 1 − e/eᵉ, so the bound is now tight: about 82% is both possible and the best possible. For a fixed number n of independent arrivals, they get the same guarantee up to a small additive loss that shrinks like 1/√n.

The key idea is a surprising equivalence. Matching Poisson arrivals turns out to be exactly the same problem as scheduling jobs whose timing is exponentially random, preserving both how the online strategy performs and what the hindsight optimum is. They design an optimal policy for the scheduling version and carry its guarantee back to matching.

They also show that if the arrival law is unknown, the best achievable ratio is strictly lower than 1 − e/eᵉ. Knowing the pattern of arrivals is worth something real.

## The catch

This is a preprint and hasn't been peer reviewed. The result is for unweighted matching (every match counts equally) and a known arrival law; real platforms weigh matches by distance, price and time. The 82% is a worst-case-style guarantee against hindsight, not a measured success rate for any real app.
{: .catch}

Matching on the spot has a hard ceiling, and now we know a strategy that hits it.
