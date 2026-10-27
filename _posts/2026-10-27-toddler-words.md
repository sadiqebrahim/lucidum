---
date: 2026-10-27 14:10:00 +0530
title: How toddlers learn "ball" without anyone pointing
dek: An old idea says children learn words by keeping a running tally of what's in view each time they hear one. Models trained on 2,441 hours of head-camera video from 48 children show it works, with help.
topic: Brain
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-27-toddler-words/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Scaling cross-situational word learning on children's naturalistic experiences, M. C. Frank, A. W. M. Tan, K. L. Aw, R. Z. Sparks et al., arXiv 2610.31842 (22 Oct 2026)"
    url: https://arxiv.org/abs/2610.31842
    note: (preprint)
---

Most of a toddler's first words are simple names for things: ball, cup, duck. But nobody holds up a ball and says "ball" every time. The word turns up in the park, the kitchen and the bath, surrounded by other things. How does a child work out which thing it means? A [new study](https://arxiv.org/abs/2610.31842) tests one answer on real children's everyday experience.

## Keep a running tally

The idea is called cross-situational learning. Each time a word is heard, note what's in view. Any single moment is ambiguous, but across many moments the right pairing keeps turning up, and it wins. Statistical information about many word meanings can, in principle, be recovered this way.

![A grid of tallies: each time "ball", "cup" or "duck" is heard, marks go to the objects in view; the matching pairs pile up.]({{ '/assets/posts/2026-10-27-toddler-words/tally.png' | relative_url }})
*Across many moments, the right word-object pairs pile up the most marks (schematic).*

## Testing it on real life

Contrastive vision-language AI models, which learn to match pictures with words, make it possible to test this strategy on what children actually see and hear. Earlier work on small data sets was a proof of concept. Michael C. Frank, Bria Long and colleagues scaled it up using the BabyView corpus: <mark>2,441 hours of video from head cameras worn by 48 children</mark>, recorded over time.

## What the models learned

Models trained on this data did learn which labels go with which objects. Two findings stand out.

First, the visual side mattered enormously. Performance was far higher when the models used visual representations pretrained on internet images than when their vision was learned only from the children's videos.

Second, most of the learning signal came from a small proportion of utterances: the ones that described something the child could actually see.

The models' word knowledge showed recognisable human-like structure. But how their performance grew with experience followed substantially different paths from those seen in children.

## The catch

This is a preprint and hasn't been peer reviewed. The models are a test of a learning strategy, not a description of what happens in a child's brain, and they only work well with vision borrowed from internet data. The authors conclude that cross-situational learning is viable for early nouns, but that developmentally plausible models will need to learn good vision from naturalistic data.
{: .catch}

Keeping a tally works for first words, but a child's eyes still do something the models can't.
