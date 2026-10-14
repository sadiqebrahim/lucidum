---
date: 2026-10-13 23:51:00 +0530
title: Debunking a fake post can help it spread
dek: A new model of online disinformation finds that debunking cuts the reach of catchy fakes but can carry weak, unappealing ones to people who would never have seen them.
topic: Social science
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-13-debunk-spread/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Modelling the complex dynamics of online disinformation cascades, Guillermo Romero Moreno, Valentin Robu and Han La Poutré, arXiv 2610.13839 (9 Oct 2026; submitted to Complex Networks 2026)"
    url: https://arxiv.org/abs/2610.13839
    note: (preprint)
---

You see a silly fake post and reply "this is false". It feels like the responsible thing to do. A [new model](https://arxiv.org/abs/2610.13839) of how disinformation spreads suggests that for some fakes, that reply is exactly what carries them further.

## Three things ordinary cascade models miss

Researchers have long modelled how posts cascade through social networks, borrowing ideas from epidemics. Guillermo Romero Moreno, Valentin Robu and Han La Poutré argue that disinformation has three features those models usually leave out:

- **It provokes debunking.** People don't just share or ignore a fake; they also reply to correct it.
- **Networks are uneven.** A few accounts have enormous numbers of connections and most have few.
- **Attention is limited.** Users only see so much, though recommendation algorithms can partly change what they see.

They built a model with all three and studied it with Monte Carlo simulations and mean-field mathematics, on random networks and on a real Twitter network.

## Debunking cuts both ways

For appealing fakes, the kind many people would happily share, debunking works as intended: corrections reduce how far the item travels.

For unappealing fakes, it's the opposite. An item hardly anyone would share should fizzle out on its own. But debunking replies are themselves activity, and in the model they <mark>let unappealing items reach audiences they would not otherwise reach</mark>.

![A network where one weak fake starts at a single node and the debunking replies light up a growing set of other nodes.]({{ '/assets/posts/2026-10-13-debunk-spread/spread.png' | relative_url }})
*A weak fake that hardly anyone shares, carried outwards by the replies debunking it (schematic).*

## Easy to ignite, hard to saturate

The model also shows what uneven networks do. When a few accounts are hugely connected, cascades trigger at much lower appeal, because one hub can expose a fake to many people at once. But the same structure limits final reach, because most accounts sit on the edges with few connections. The authors sum it up as "easy to ignite yet hard to saturate".

Limited attention cancels those network effects: if people only see a slice of what reaches them, a hub's reach counts for less. Recommendation algorithms that decide what people see may restore the effects.

## Why it matters

Platforms, fact-checkers and ordinary users all face the same question: should this be corrected in public? The model suggests the answer depends on the item. For a fake that is already spreading, correction helps. For one that is going nowhere, a loud public correction may be what gives it an audience.

## The catch

This is a simulation model, not a measurement of real users, and it's a preprint that hasn't been peer reviewed (it has been submitted to the Complex Networks 2026 conference). Its results depend on how appeal, debunking and attention are modelled. Real platforms also have features the model may not capture, such as quote-posts and different ways of showing replies.
{: .catch}

Before you reply to a fake that's going nowhere, it's worth asking who your correction will show it to.
