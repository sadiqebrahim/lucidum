---
date: 2026-10-19 15:00:00 +0530
title: One poll is usually enough to sink a third party
dek: A new voting model finds that, starting from honest votes, a single published poll typically pushes everyone towards the top two candidates, though sometimes the votes cycle instead of settling.
topic: Society
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-19-duverger-polls/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Trembling toward Duverger: Convergence and Cycles in Synchronous Plurality Dynamics, M. Weigel, D. Berriaud and R. Wattenhofer, arXiv 2610.23330 (16 Oct 2026)"
    url: https://arxiv.org/abs/2610.23330
    note: (preprint)
---

Your favourite party is third in the polls. Do you still vote for it? A [new model](https://arxiv.org/abs/2610.23330) suggests that, in elections where the most votes wins, one poll is usually enough to squeeze the race down to two.

## Duverger's law

Duverger's law is the observation that plurality elections ("first past the post") tend to concentrate support on two candidates. The usual explanations use "pivotal voter" models, in which two-candidate competition emerges in the limit of very large electorates, driven by uncertainty about how everyone else will vote.

## A smaller, concrete model

Maximilian Weigel, Damien Berriaud and Roger Wattenhofer instead model a fixed, finite group of voters. A poll reveals the current vote counts. Each voter then best-responds with "trembling-hand" beliefs, assuming any other voter might deviate with a small probability. In practice, that means asking where one vote could still change the result.

## One poll, then it locks

Starting from honest votes, the authors show that <mark>a single update typically suffices</mark>. The votes converge to a stable profile in which every voter supports whichever of the two poll leaders they prefer.

![A poll with two leading candidates and a trailing third; after one poll, votes lock onto the top two.]({{ '/assets/posts/2026-10-19-duverger-polls/one-poll.png' | relative_url }})
*After one poll, voters move to whichever of the top two they prefer (schematic).*

The condition is small. For any number of candidates, a lead of four votes for the runner-up over every lower-placed candidate is enough; with three candidates, a lead of two suffices. With random preferences, Duverger's law emerges after one update with probability 1 − O(N^−1/2), which approaches certainty as the electorate grows.

## When it doesn't settle

Convergence can fail. Mild cycles of period two appear, with a few voters swapping ballots around an otherwise stable outcome. Richer behaviour is possible even with three candidates: period-three cycles involving six voters (no such cycle can involve fewer than four), cycles that alternate the winner, and, in larger electorates, cycles of any odd length.

## The catch

This is a theoretical model and a preprint, not yet peer reviewed. Real voters don't all best-respond to a single poll at the same moment, and real polls are noisy. The model shows how quickly strategic voting can work, not how any particular election will go.
{: .catch}

When the most votes wins, one poll can decide who's really in the race.
