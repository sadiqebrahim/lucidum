---
date: 2026-09-29 11:18:00 +0530
title: Teaching AI to know when it's sure
dek: Fine-tuning reasoning models on just 600 problems to predict their own confidence, with nothing in the training about length, made them write up to 25% less at the same accuracy.
topic: AI
format: explainer
review_status: preprint
thumb: /assets/posts/2026-09-29-ai-confidence/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Learning to Stop without Learning to Stop: Self-Supervised Confidence Training Improves Reasoning Efficiency, Hosseini et al., arXiv 2609.31619 (2026)"
    url: https://arxiv.org/abs/2609.31619
    note: (preprint, CC BY 4.0)
---

The newest AI models "think out loud" before they answer, writing out long chains of reasoning, sometimes thousands of words, and every word costs time and energy. A new preprint from the University of Maryland and Capital One finds a surprisingly indirect way to make them stop sooner: <mark>teach them to judge how sure they are</mark>, and nothing else. Their reasoning got up to 25% shorter, with no loss of accuracy.

## How sure is the AI, mid-thought?

The researchers, led by Parsa Hosseini, first looked at how models reason. They let a model think, stopped it at points along the way (each time it wrote "Wait", a common pause in reasoning models), asked for its answer so far, and measured how confident it was in that answer.

![A line of thought paused midway; the AI is asked for its answer so far, x = 12, and a gauge shows it is 64% sure.]({{ '/assets/posts/2026-09-29-ai-confidence/pause.png' | relative_url }})
*Pause, ask for the answer so far, and measure how sure the model is.*

Confidence here has a precise meaning. A language model assigns a probability to every word it produces. For the trial answer, the team takes the average of those probabilities (a geometric mean, the natural average for probabilities that multiply together):

![The equation c equals the exponential of the average log probability of each word in the answer, with an example of a confident answer at 92% and a guessing one at 34%.]({{ '/assets/posts/2026-09-29-ai-confidence/confidence.png' | relative_url }})
*c = exp((1/n) Σ log pᵢ): the geometric mean of the probabilities of the answer's words. The example bars are illustrative.*

The score comes entirely from the model's own probabilities; no one needs to know the right answer. And it carries useful information: the team found that extra reasoning helps most when the model is unsure, and barely helps at all once it is confident.

## The only lesson: predict your own confidence

Instead of using that score to cut the model off, the researchers asked what happens if the model simply learns to predict it. Their method, which they call ConfSFT, generates reasoning from the model itself, computes the confidence at each pause, and fine-tunes the model to write that confidence as a percentage. Only 600 training problems were used.

Crucially, the training contains no reward for shorter reasoning and no instruction to stop early, and at run time the model generates normally, with no confidence check and no stop button.

## What happened

Yet the fine-tuned models reasoned more efficiently: they produced up to 25% fewer tokens (the word pieces models write) at matched accuracy, across four families of open models (Gemma, Qwen, Nemotron and GPT-OSS) on maths, science and coding benchmarks. The gains were comparable to methods that explicitly train for shorter reasoning, and the models' overall style of reasoning stayed largely the same rather than dropping particular steps.

![Reasoning length before, and after up to 25% shorter, with the same accuracy, across Gemma, Qwen, Nemotron and GPT-OSS on maths, science and coding.]({{ '/assets/posts/2026-09-29-ai-confidence/result.png' | relative_url }})
*Best case shown: up to 25% fewer tokens at the same accuracy.*

## Why it matters

Reasoning models are expensive to run, and much of that cost is thinking that doesn't change the answer. If efficiency can come as a side effect of teaching a model to know what it knows, it is a cheap fix: a small fine-tune, no new inference machinery. The authors suggest that efficient reasoning may emerge from learning this kind of self-knowledge rather than from being optimised directly.

This is a preprint and hasn't been peer-reviewed. "Up to 25%" is the best case; savings vary by model and benchmark. The tests used open models and standard benchmarks, and it isn't yet known how the approach holds up in the largest commercial systems or on everyday tasks.
{: .catch}

An AI that learns to tell when it's sure also seems to learn when to stop thinking.
