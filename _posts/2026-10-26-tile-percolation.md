---
date: 2026-10-26 12:40:00 +0530
title: When does water get across the floor? Tipping points for 23,396 tilings
dek: Percolation is the moment a path suddenly opens all the way across. A new study computes that tipping point for every tiling made of regular shapes up to a size limit, and finds a shortcut that predicts most of them.
topic: Physics
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-26-tile-percolation/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Site and bond percolation thresholds of all k-uniform tilings with k≤10, Maksim Elisov, arXiv 2610.31190 (Oct 2026)"
    url: https://arxiv.org/abs/2610.31190
    note: (preprint)
---

Imagine water seeping across a tiled floor, tile by tile, through only the tiles that are already wet. With few wet tiles, it never gets far. Add more, and at some point a path suddenly opens from one side to the other. On a square grid that happens when about 59% of the tiles are wet. A [new study](https://arxiv.org/abs/2610.31190) computes that tipping point for tens of thousands of other patterns.

## Percolation: all at once

This is percolation, a model physicists use for everything from fluids moving through rock to the spread of disease. Its key feature is a sharp threshold. On a large grid, below the critical share you almost never get a connected path across; just above it, you almost always do. It isn't a slow rise. It's a switch.

The wet tiles are our way of picturing it. In the maths, the "sites" are the corners where the lines of a grid meet (site percolation), or the lines themselves (bond percolation), and each is open at random with some probability.

## Every tiling has its own threshold

Maksim Elisov looked at k-uniform tilings: ways of covering a flat plane with regular polygons, such as triangles, squares and hexagons, sorted by how many different kinds of corner (k) they contain. He computed site and bond thresholds for <mark>all 23,396 such tilings with k up to 10</mark>.

![Three grids: square with threshold 0.593, triangle exactly one half, honeycomb about 0.697.]({{ '/assets/posts/2026-10-26-tile-percolation/tilings.png' | relative_url }})
*Site thresholds for three familiar grids: square 0.593, triangle exactly ½, honeycomb ≈ 0.697 (schematic patches).*

For the 486 tilings with k up to 4, the thresholds are given to about six decimal places. The method reproduces the known values for the 22 classic Archimedean lattices, which is a useful check. For example, on the square grid the site threshold comes out as 0.5927452, against a reference value of 0.5927460508. On the triangular grid it is exactly ½, and on the honeycomb about 0.697.

## A shortcut: count the corners

The paper also finds a simple predictor. Knowing just the mix of corner types in a tiling, the fraction of each kind of vertex, fixes the threshold for tilings with k of 5 or more to within about 0.002. It isn't perfect: tilings with the same mix of corners can differ by up to 0.006 for site percolation and 0.02 for bond percolation.

## The catch

This is a preprint and hasn't been peer reviewed. The thresholds are computed numerically, not proven, and the floor-and-water picture is only an analogy for the grid maths. The shortcut is an approximation that works well for most tilings, not an exact rule.
{: .catch}

A network's shape sets its tipping point, and its corners tell you most of it.
