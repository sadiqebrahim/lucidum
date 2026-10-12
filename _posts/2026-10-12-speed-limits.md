---
date: 2026-10-12 10:07:00 +0530
title: Two unbeatable computing speed limits, beaten
dek: Josh Alman and Virginia Vassilevska Williams report the first polynomial speed-ups for 3SUM and all-pairs shortest paths, refuting two hypotheses that a whole branch of complexity theory was built on.
topic: Deep tech
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-12-speed-limits/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Truly Subquadratic 3SUM and Truly Subcubic APSP via Triangles in Sparse Lopsided Graphs, Josh Alman and Virginia Vassilevska Williams, arXiv 2610.06783 (5 Oct 2026)"
    url: https://arxiv.org/abs/2610.06783
    note: (preprint)
---

For decades, computer scientists have treated two simple problems as having speed limits nobody could meaningfully beat, and they built a whole theory of which problems are hard on top of them. In a [76-page preprint](https://arxiv.org/abs/2610.06783), Josh Alman and Virginia Vassilevska Williams say they have broken both.

## Two puzzles

**3SUM.** You get a list of n whole numbers. Are there three that add up to zero? The textbook method takes roughly n² steps: for every pair, you check whether the number that would complete it is in the list.

**All-pairs shortest paths (APSP).** You get a map of n points with weighted roads between them. Find the shortest route between every pair. The textbook method takes roughly n³ steps.

Decades of work have shaved off smaller factors, such as powers of logarithms, but never a fixed power of n. That led to two working assumptions. The 3SUM hypothesis says no algorithm runs in n^(2−ε) time for any fixed ε > 0. The APSP hypothesis says the same for n^(3−ε).

## Why everyone cared

These hypotheses became foundations for a field called fine-grained complexity. If you could show that a fast algorithm for problem X would also give a fast 3SUM or APSP algorithm, you had strong evidence that X was hard too. Many problems in geometry, graphs and data structures got their "probably can't do better" labels this way.

## The new result

Alman and Vassilevska Williams give deterministic algorithms that solve:

- 3SUM on n integers of polynomial size in O(n^1.9992) time;
- APSP on directed n-vertex graphs with polynomially bounded integer weights in O(n^2.9995) time.

![3SUM goes from n squared to n to the 1.9992, and APSP from n cubed to n to the 2.9995.]({{ '/assets/posts/2026-10-12-speed-limits/bounds.png' | relative_url }})
*The new exponents sit just below the old limits, but strictly below.*

The exponents are only a hair below 2 and 3, but they are strictly below, and that is exactly what the hypotheses said couldn't happen. Using known reductions, the authors say the result also refutes the real-valued versions of both hypotheses, the Exact Triangle hypothesis, the Zero-Weight k-Clique hypotheses and three Online Matrix–Vector conjectures, and speeds up a range of other problems.

## How they did it

Everything comes from one new algorithm for a narrow kind of matrix multiplication. When one matrix is very thin, and you only need some of the entries of the product rather than all of them, they show you can compute those entries with fewer operations than it would take to write the full product down. They build it by modifying a variant of Coppersmith's rectangular matrix-multiplication method, which rests on a ten-multiplication identity of Schönhage. Read as a graph problem, it finds triangles fast in sparse, lopsided graphs, and known reductions carry that speed-up back to 3SUM and APSP.

## The catch

This is a preprint and has not been peer reviewed. A 76-page proof will take experts time to check. The practical gain is tiny: going from n² to n^1.9992 matters for theory, not for anyone's code today. The results also apply to whole-number inputs of bounded size, not to every version of these problems.
{: .catch}

The speed-up is small, but <mark>a speed limit only has to fail once</mark>, and theorists now have to decide what fine-grained hardness should rest on instead.
