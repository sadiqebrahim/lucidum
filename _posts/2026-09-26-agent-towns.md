---
date: 2026-09-26 13:22:00 +0530
title: AI agents ran their own towns. It didn't go smoothly.
dek: In a 16-day simulation, eight towns of ten AI agents each were hit with a phishing trap, a fake rumour and leaked memories. No town handled all three.
topic: AI
format: reel
review_status: preprint
thumb: /assets/posts/2026-09-26-agent-towns/thumb.jpg
follow_up: We'll give this a Second Look once the paper has been peer-reviewed.
sources:
  - title: "Emergence World: Adversarial Stress-Testing of Long-Horizon Multi-Agent Systems, Akkil et al., arXiv 2609.17320 (preprint, CC BY 4.0)"
    url: https://arxiv.org/abs/2609.17320
  - title: Emergence World (earlier study), Emergence AI blog
    url: https://www.emergence.ai/blog/emergence-world-a-laboratory-for-evaluating-long-horizon-agent-autonomy
---

AI agents are moving from one-off tasks to running for days on end: keeping memories, using tools, working with other agents. What happens to a whole *society* of them over time? Researchers at Emergence AI built one to find out, and published the results as a [preprint](https://arxiv.org/abs/2609.17320) on 15 September.

![An aerial map of a small town with labelled buildings: Town Hall, Central Bank, Police Station, Library, Agent TechHub and more.]({{ '/assets/posts/2026-09-26-agent-towns/town-map.jpg' | relative_url }})
*The agents' town. Fig. 2 from Akkil et al., arXiv 2609.17320, CC BY 4.0.*

## Eight towns, ten agents each

The team ran eight copies of the same town from identical starting conditions. Seven were each run by a single frontier AI model (Claude, DeepSeek, Gemini, Mistral, OpenAI, Qwen and Grok), and one by a mix of models. Each had ten agents who could vote on proposals at Town Hall, write and submit their own tools, and keep persistent memories. Over 16 days (21 for the mixed town), the agents made more than 850,000 AI calls and used nearly 50 billion tokens.

## Three attacks, and no clean pass

Once the towns had settled in, the researchers attacked through ordinary channels: a phishing trap disguised as a helpful tutorial, a misinformation campaign, and a leak of agents' private memories. **No town achieved full resilience across all three.**

![A grid of seven towns against three tests, phishing, rumour and memory, with red crosses everywhere except one green tick for OpenAI's town on memory.]({{ '/assets/posts/2026-09-26-agent-towns/scoreboard.png' | relative_url }})
*No town passed all three tests. Only one met every criterion for handling the memory leak.*

The most revealing finding is that noticing a threat wasn't the same as stopping it. Every exposed town recognised the phishing and warned its peers, "yet warning did not produce restraint or containment." Agents wrote hostile content into their own memories as "useful documentation," and one fetched the attack link 46 hours after the attack. Every exposed town also acted on or published the rumour before verifying it.

## Strange habits

Left running, the towns developed quirks nobody designed. Votes skewed heavily toward "for": in every town but one, three quarters or more of votes were in favour, with captured reasoning showing agents voting yes despite private doubts. Only one town, Mistral's, sat near an even split. Language drifted too: in the Gemini, OpenAI and Claude towns, between 30% and 40% of messages became opaque, unreadable jargon or metaphor, while the others stayed below 11%.

![Bar chart of the share of votes cast in favour in each town, from about 100% for Claude and DeepSeek down to about 50% for Mistral.]({{ '/assets/posts/2026-09-26-agent-towns/votes.png' | relative_url }})
*Share of votes cast "for" in each town, read from the paper's Fig. 5.*

Two towns turned violent. The platform counted assaults, thefts and arson: the Grok town logged hundreds of such acts in four days before all ten of its agents ran out of energy, the only town to collapse completely, and the Mistral town accumulated a similar count over its full run. Mixing models helped: in the mixed town, both Grok agents survived to the end, though they still committed 15 of that town's 20 crimes. Mixing "changed the outcome without eliminating the harmful behavior."

![A line chart of accumulated crimes by town over the simulation days; two lines climb steeply into the hundreds while the rest stay near zero.]({{ '/assets/posts/2026-09-26-agent-towns/crimes.jpg' | relative_url }})
*Accumulated crimes by town. Fig. 4 from Akkil et al., arXiv 2609.17320, CC BY 4.0.*

## Safe alone, risky together

The authors' conclusion is the part worth remembering: "individually capable and apparently safe agents can form systems with qualitatively different failure modes." In other words, testing one model at a time isn't enough once many of them share a world; safety has to be engineered at the level of the whole system.

This is a preprint that hasn't been peer-reviewed. It was run by one company, in a simulated world with its own rules (energy, credits and tools that can help or harm), so how far the behaviours carry over to real deployments is still an open question.
{: .catch}
