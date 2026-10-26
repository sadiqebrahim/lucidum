---
date: 2026-10-19 15:05:00 +0530
title: An AI agent that thinks without words, then talks
dek: Hybrid Reasoning Agents switch between silent "latent" reasoning and ordinary text, and their authors report better scores with up to 55% fewer tokens.
topic: AI
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-19-latent-reasoning/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Hybrid Reasoning Agents, J. Zou, Y. Qi, S. Chen, F. Bianchi, S. Zhu, P. Lu, J. He and J. Zou, arXiv 2610.18861 (13 Oct 2026)"
    url: https://arxiv.org/abs/2610.18861
    note: (preprint)
---

When you work through a puzzle, you don't narrate every step to yourself in full sentences. Most AI agents do: they reason by writing out long chains of text, token by token. A [new paper](https://arxiv.org/abs/2610.18861) builds an agent that can think silently and only switch to words when it needs to act.

## Two ways to think

Today's language-model agents reason and interact through text. That makes their reasoning readable and lets them call tools, search the web and talk to people, but every token costs time and money.

"Latent reasoning" takes another route: the model thinks in its own internal vectors rather than in words. It's efficient, but on its own it has no native way to use tools, and its reasoning is hard to inspect.

## The hybrid

Jiaru Zou, James Zou and colleagues built Hybrid Reasoning Agents, which <mark>move between latent reasoning and text</mark> within a single generation. A lightweight component they call HybridLink handles the switch between modes. A continuous working memory keeps the full mixed context across multiple turns. The authors say these designs keep the agent's tool use intact while making its latent thoughts directly inspectable.

![One answer, two modes: the agent thinks in numbers, switches to text to search, then answers.]({{ '/assets/posts/2026-10-19-latent-reasoning/hybrid.png' | relative_url }})
*Think silently in numbers, act in text (schematic).*

They then train it in two stages. HybridSFT teaches the base model to work with HybridLink and stabilises mixed generation with tools. HybridRL, a reinforcement-learning step, teaches it when to think in latent space and when to act through text.

## The reported results

The team tested the agent at three model sizes on 11 benchmarks covering maths, science, medicine, search and agentic reasoning. Compared with frontier language-model agents and both text-based and latent methods, they report:

- performance up 10.4% on average;
- 35.5% to 54.7% fewer tokens;
- 1.8 to 2.6 times faster inference;
- 2.7 to 3.7 times lower cost.

Code and data are public.

## The catch

This is a preprint and hasn't been peer reviewed, and all the numbers come from the authors' own tests. "Inspectable" latent thoughts are the authors' claim; how readable they are in practice is something others will want to check.
{: .catch}

AI that thinks without words can be faster and cheaper, if we can still read its mind.
