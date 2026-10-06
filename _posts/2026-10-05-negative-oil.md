---
date: 2026-10-05 23:50:00 +0530
title: How oil fell to minus $37 a barrel
dek: A new feedback model shows how traders forced to close positions before delivery can push a futures price below zero, as happened to US oil on 20 April 2020.
topic: Economics
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-05-negative-oil/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Negative Oil & Nickel Squeeze: A Feedback Model for Extreme Commodity Futures Prices, Zimbidis & Sircar, arXiv 2610.00951 (1 Oct 2026)"
    url: https://arxiv.org/abs/2610.00951
    note: (preprint)
---

On 20 April 2020, oil cost less than nothing. The May contract for West Texas Intermediate (WTI) crude, one day before it expired, opened near $17 a barrel, fell to an intraday low of −$40.32 and settled at −$37.63. Sellers were, in effect, paying buyers to take oil away. A [new paper](https://arxiv.org/abs/2610.00951) by Iosif Zimbidis and Ronnie Sircar offers <mark>a model in which that can actually happen</mark>.

![A schematic of the 20 April 2020 price path, falling from about $17 to a low of −$40.32 and closing at −$37.63.]({{ '/assets/posts/2026-10-05-negative-oil/crash.png' | relative_url }})
*The day in outline (shape schematic; the three prices are real).*

## Why a price can be forced down

An oil futures contract is a promise to take real barrels at a set place and time. As expiry approaches, traders who can't take physical delivery must close their positions, whatever the price. The paper argues that these constraints on physical delivery create pressure that distorts the futures price, and that the same mechanism explains the March 2022 nickel squeeze, when prices spiked rather than crashed.

## The feedback model

Standard pricing models treat the price as positive by construction. This model adds feedback: the price traders see includes a correction that depends on the imbalance between delivery-constrained long and short positions, and that correction behaves like a "roll option". Because the option's payoff depends on the observed price, which itself contains the correction, the pricing equation becomes nonlinear.

![A loop: forced selling makes the price drop, and the lower price feeds back into more forced selling.]({{ '/assets/posts/2026-10-05-negative-oil/feedback.png' | relative_url }})
*Forced selling and price feed each other.*

Remarkably, the authors find an explicit solution in terms of the classical Black-Scholes-Margrabe formulas, the ones used to price an option to swap one asset for another, up to solving a single equation. With enough distortion, even a model built on always-positive prices produces negative ones. Applied to WTI and nickel, the model estimates how large the position imbalance had to be to produce the extreme moves.

## Why it matters

Negative prices and squeezes caught markets by surprise. A model that links them to measurable position imbalances, with a closed-form answer, gives traders and regulators a way to see such events coming and to size the risk.

This is a preprint and hasn't been peer-reviewed. The model is a stylised description fitted to two events; whether it can forecast the next one in advance hasn't been shown.
{: .catch}

When traders are forced out all at once, a price can break below zero, and now there's a formula for when.
