---
date: 2026-10-12 10:06:00 +0530
title: Quantum's magic square breaks with three players
dek: Entangled pairs win the magic square game every time, but a new paper finds that with three or more players the quantum strategy wins only a third to three quarters of the time, below the classical 8 in 9.
topic: Quantum computing
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-12-magic-square/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "The Mermin-Peres Magic Square Game With Three or More Players, Itamar Lorian and J. E. Avron, arXiv 2610.06534 (5 Oct 2026)"
    url: https://arxiv.org/abs/2610.06534
    note: (preprint)
---

There is a puzzle that two players who can't talk to each other can win every single time, but only if they share quantum entanglement. It's one of the neatest demonstrations that the quantum world beats anything classical. A [new paper](https://arxiv.org/abs/2610.06534) asks what happens when you add a third player, and finds that the magic breaks.

## The game

The Mermin-Peres magic square game uses a three-by-three grid. A referee gives Alice one row and Bob one column. Each fills in their three squares with +1 or −1, following two rules: Alice's row must multiply to +1, and Bob's column must multiply to −1. They win if they put the same value in the one square where their row and column cross.

They can agree a strategy in advance, but once the game starts they can't communicate.

![A three-by-three grid. Alice fills the middle row, Bob fills the middle column, and the shared square is highlighted.]({{ '/assets/posts/2026-10-12-magic-square/game.png' | relative_url }})
*Alice fills a row, Bob fills a column. They win if they agree on the square where the two cross.*

## Why classical players top out at 8 in 9

The obvious plan is to write down one complete grid in advance and both copy from it. But no such grid exists. Multiply all nine numbers by rows and you get (+1)³ = +1. Multiply them by columns and you get (−1)³ = −1. The same nine numbers can't give both answers, so any fixed grid breaks at least one of the six rules. The best a classical team can do is get 8 of the 9 row–column pairs right: a win probability of 8/9.

## How entanglement wins every time

Give Alice and Bob two entangled pairs of particles before the game, and each can fill in their squares by measuring their own particles in a way that depends on the row or column they were given. Quantum mechanics guarantees the rules are always met and the shared square always matches. They win every time, with no communication, which classical physics says should be impossible.

## Adding players

Itamar Lorian and J. E. Avron generalise the game to N players. The square becomes a cube for three players, and an N-dimensional hypercube beyond that. They show two things:

- The best classical strategy still wins 8/9 of the time, for every N.
- For three or more players, the natural generalisation of the quantum strategy wins only between 1/3 and 3/4 of the time.

So with three or more players, the quantum strategy is not just weaker than before. It does <mark>worse than playing classically</mark>.

## Why: entanglement is monogamous

The authors trace the loss to monogamy of entanglement. If two particles are maximally entangled with each other, neither can share strong entanglement with a third. The two-player trick depends on perfect correlations between pairs, and in the bigger game every player needs to be tightly correlated with several others at once. Entanglement can't be spread that way.

## The catch

This is a preprint and hasn't been peer reviewed. The 1/3–3/4 range applies to the specific generalisation of the two-player quantum strategy the authors study. The abstract doesn't claim that no cleverer quantum strategy could do better with three or more players.
{: .catch}

Quantum teamwork is real, but it doesn't scale for free: one strong link can't be shared around the table.
