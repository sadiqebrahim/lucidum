---
date: 2026-10-01 11:10:00 +0530
title: The 1-in-e rule for saying yes, finally settled
dek: The famous 37% rule tells you when to stop looking for the best candidate. A new proof says the same guarantee holds when you are picking a whole team.
topic: Maths
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-01-secretary/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Settling the Matroid Secretary Problem, Zhiyi Huang, arXiv 2609.30421 (24 Sep 2026)"
    url: https://arxiv.org/abs/2609.30421
    note: (preprint)
---

You're interviewing people one at a time. After each interview you must say yes or no on the spot, and you can't go back. When should you stop? Mathematics has a famous answer. A [new paper](https://arxiv.org/abs/2609.30421) says it scales up from one choice to a whole team.

## The 37% rule

This is the "secretary problem". The classic strategy: let the first 37% of candidates go, however good they look, and just note the best of them. Then hire the first person who beats everyone you've seen.

Do that and you land the single best candidate about one time in *e* (*e* ≈ 2.718), which is roughly 37%. It's proven that no strategy does better.

![A curve of the chance of picking the best against the share of people you let go first, peaking at 37%.]({{ '/assets/posts/2026-10-01-secretary/peak.png' | relative_url }})
*Your chance of landing the best peaks when you let the first 37% go.*

## The hard version: a whole team

Real choices are often bigger. You might be filling several roles at once, with rules about which combinations of people can work together. Mathematicians capture rules like these with a structure called a matroid, and the question became the matroid secretary problem. It was posed in 2007 and has stayed open since.

The question was whether some strategy could match the 1-in-*e* guarantee for every member of the best possible team, whatever the matroid.

## The claimed answer

Zhiyi Huang of the University of Hong Kong has posted a paper titled "Settling the Matroid Secretary Problem". It describes an algorithm that is <mark>e-probability-competitive</mark>: each member of the optimal team is hired with probability at least 1/*e*.

The algorithm is "ordinal", meaning it only compares candidates with each other rather than using their exact scores. It checks whether a group is allowed through a standard test (an independence oracle), and it runs in expected polynomial time, so it is practical to compute.

## The catch

This is a preprint and hasn't been peer reviewed. A proof that closes a 19-year-old problem will be checked closely by other mathematicians before it's accepted. The abstract is short and gives no worked examples, so we've kept to what it states.
{: .catch}

If the proof holds, the 1-in-*e* rule works for whole teams too.
