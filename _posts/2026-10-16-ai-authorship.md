---
date: 2026-10-16 23:22:00 +0530
title: A few random codes make AI writing look human
dek: A leading way to score how much of an AI-assisted text is really yours can be gamed by asking the AI to copy a few random IDs, swinging the same text between 15% and 85% "human".
topic: AI
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-16-ai-authorship/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Likelihood Is Not Authorship: Can We Reliably Measure Human Contribution in AI-Assisted Writing?, Hasan Amin, Zhuoran Lu and Ming Yin, arXiv 2610.19767 (14 Oct 2026)"
    url: https://arxiv.org/abs/2610.19767
    note: (preprint)
---

As AI becomes a normal part of writing, the question shifts from "did you use AI?" to "how much of this is yours?" A [new paper](https://arxiv.org/abs/2610.19767) shows that a prominent way of answering it can be gamed with a trick: ask the AI to copy a few random codes, and <mark>the same text can score 85% human instead of 15%</mark>.

## The measure

One line of work estimates human contribution by asking how predictive your prompt is of the final text. The idea is intuitive: if you supplied a detailed prompt full of your own ideas, the output follows from you, so more of it counts as yours. A vague prompt means the model did more of the work.

## The trick: specificity padding

Hasan Amin, Zhuoran Lu and Ming Yin introduce what they call specificity padding. Put a few random IDs in the prompt and ask the model to copy them into the text. That alone makes a title-only request look more human than a prompt that supplies the article's key ideas.

They then ran a "context swap" audit. They kept each document fixed and only showed or hid the IDs to the evaluator. The score of the unchanged text swung by a third to half of its scale, and it went up for every document they tested. That held for news articles and scientific abstracts, and across language models from 3.8 billion to 753 billion parameters. The same articles could average 85% human or 15% human depending only on which prompt was on record. Even with no prompt at all, the output-only variant of the score rewarded the random strings themselves.

![A bar chart of per-word credit in which an ordinary word gets a small bar and a random ID string gets a very tall one, under the formula: score is a sum of word contributions weighted by surprise.]({{ '/assets/posts/2026-10-16-ai-authorship/ledger.png' | relative_url }})
*The score is a surprisal-weighted average, so rare strings soak up the credit (schematic).*

## Why it happens

The authors derive an exact identity they call the credit ledger. The score is a surprisal-weighted average over the text. Rare strings, ones that would be very surprising without the context, carry big weights. If the context makes them easy to copy, they collect the credit, whatever they mean.

They also prove a deeper limit, a two-point bound. If the prompt itself could have been machine-written, then in the worst case every method that only looks at the transcript must miss by half of the contribution at stake.

## The catch

This is a preprint and hasn't been peer reviewed. It's about one family of measures, the ones based on how likely the text is given the prompt, not about every AI detector. The authors don't say human contribution can't be measured at all. They say likelihood scores alone can't establish it without evidence of what the person added and how the text was produced.
{: .catch}

A number that says "85% you" is only as good as what it actually measured.
