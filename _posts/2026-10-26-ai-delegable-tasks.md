---
date: 2026-10-26 12:50:00 +0530
title: The tasks AI agents take over first are the 12-minute ones
dek: An open index of nearly 19,000 job tasks finds about a third of the world's work time could be partly handed to AI agents, but only 2.5% fully, and rich countries are twice as exposed as poor ones.
topic: AI
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-26-ai-delegable-tasks/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "The Delegation Divide: An Open Index of AI-Agent Delegability across Occupations and Countries, Espinal Maya and Jiménez Londoño, arXiv 2610.30752 (Oct 2026)"
    url: https://arxiv.org/abs/2610.30752
    note: (preprint, preregistered, CC BY 4.0)
---

Which parts of your job could an AI agent take off your hands? A [new open index](https://arxiv.org/abs/2610.30752) tries to answer that for nearly every task in the economy, and finds that the answer is less about how hard a task is than about how long it takes.

## The index

Two researchers rated 18,796 task descriptions from O*NET, the US occupational database, for how much an AI agent could carry them out. The ratings were made by AI models using a fixed rubric that was preregistered, set out in advance. They then mapped the tasks onto 433 international occupation groups and weighted them by the jobs in 146 countries.

## Partly, yes. Fully, rarely

In 2026, about <mark>35.2% of the world's task time</mark> is at least partly delegable to AI agents, by their measure. Only 2.5% is fully delegable.

## Not the hardest, the 12-minute ones

You might expect AI to take the hardest work first. Instead, full delegation peaks for tasks that take a person about 11.8 minutes. Short, well-defined tasks are the ones agents can most often complete end to end; long, complex ones rarely are.

## A divide between countries

Exposure rises with national income. In low-income countries, 22.5% of work time is at least partly delegable; in high-income countries, 48.7%. Each log point of GDP per person adds about 7.2 percentage points. In poorer countries, physical work is the main barrier.

![Bars: 35.2% of work time partly delegable, 2.5% fully; high-income countries 48.7% against 22.5% in low-income countries.]({{ '/assets/posts/2026-10-26-ai-delegable-tasks/divide.png' | relative_url }})
*About a third partly, very little fully, and a wide gap between rich and poor countries.*

## Does it match reality?

The authors ran several checks. The index correlates strongly with earlier AI exposure measures (r = 0.93 and 0.89). Across 101 countries it tracks observed AI usage (r = 0.86). The model ratings agreed with each other (kappa 0.77), with human raters on a sample of 300 tasks (0.85) and with an agentic panel (0.87). One preregistered idea, an "adoption gap" between where AI could be used and where it is, was not supported (p = 0.27).

## The catch

This is a preprint and hasn't been peer reviewed. The index measures what <em>could</em> be delegated, not what will be, or whether jobs will disappear. The ratings come mostly from AI models judging task descriptions, checked against humans on a sample.
{: .catch}

AI agents take tasks, not whole jobs, and the 12-minute tasks go first.
