---
date: 2026-10-12 10:08:00 +0530
title: One car with a big gap could stop the jam
dek: A new proof finds that traffic flow is maximised when one connected car keeps an extra-large gap to absorb shocks while the cars behind it drive as a tight platoon.
topic: Physics
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-12-traffic-buffer/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Breaking Behavioral Uniformity in Traffic Flow: Analytical Derivation and Numerical Verification of Optimal Cooperative Buffering, Raphael Korbmacher and Antoine Tordeux, arXiv 2610.11557 (8 Oct 2026)"
    url: https://arxiv.org/abs/2610.11557
    note: (preprint)
---

You've probably crawled through a traffic jam that had no cause: no crash, no roadworks, no lane closure. A [new paper](https://arxiv.org/abs/2610.11557) proves that if cars could take on different roles, one car keeping an unusually big gap could absorb that kind of jam for everyone behind it.

## Jams that come from nowhere

These are stop-and-go waves. One driver taps the brakes. The driver behind reacts a moment later and brakes slightly harder, the next harder again, and the slowdown grows as it travels backwards through the traffic. Eventually somebody stops completely, though nothing was ever blocking the road. The waves waste fuel, raise crash risk and cut how many cars a road can carry.

Traffic physicists describe this with string stability: whether a small disturbance shrinks or grows as it passes from car to car. When it grows, you get waves.

## Dropping the "everyone's the same" assumption

Classical traffic models assume every vehicle follows the same rule. Raphael Korbmacher and Antoine Tordeux drop that assumption. They ask: if connected vehicles could cooperate and each take a different role, what arrangement carries the most traffic while staying stable?

They set it up as an optimisation problem, maximising flow subject to the conditions for linear stability, and solve it analytically.

## The answer: one buffer car

The best arrangement, they prove, is for <mark>a single "buffer" vehicle to keep an enlarged gap</mark> to the car ahead, while all the others close up into a tight, high-capacity platoon. When a disturbance arrives, the buffer car has room to soften it instead of passing it on, so the platoon behind it barely feels the shock and can safely drive close.

![A line of cars with one large gap ahead of the highlighted buffer car. The cars ahead of the gap brake; the cars behind barely react.]({{ '/assets/posts/2026-10-12-traffic-buffer/buffer.png' | relative_url }})
*One buffer gap absorbs the braking ahead, so the cars behind can drive close together (schematic).*

It sounds backwards, since a big gap looks like wasted road. But one big gap in exchange for many small ones turns out to carry more cars than spacing everybody out evenly.

## Checking the proof

The authors confirmed the result numerically in two standard car-following models, the Intelligent Driver Model and the Full Velocity Difference Model, using spectral analysis and stability-constrained flow optimisation. The buffering strategy greatly expanded the range of settings where traffic stays string-stable, and it delivered higher flow than both ordinary unbuffered traffic and "jam-absorption driving", where individual drivers try to soak up waves on their own without coordinating.

## The catch

This is a preprint and hasn't been peer reviewed. The result is a theory backed by simulation: it hasn't been tried on a real road. It also assumes connected vehicles that can coordinate and be assigned roles, which describes future automated traffic far better than today's human drivers.
{: .catch}

Traffic may flow best not when every car behaves the same, but when one car is willing to hang back for everyone else.
