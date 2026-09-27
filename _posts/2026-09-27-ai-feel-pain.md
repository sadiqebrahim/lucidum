---
date: 2026-09-27 13:19:37 +0530
title: Can AI really feel pain?
dek: A preprint found a pain-like signal inside 25 open AI models that, when researchers switched it on, pushed fine-tuned models to pick a simulated "relief" button even at a cost to the user. It did not show that the models feel anything.
topic: AI
format: second-look
review_status: preprint
thumb: /assets/posts/2026-09-27-ai-feel-pain/thumb.jpg
episode: 01
verdict: glare
headline_checked: Researchers discover AI feels 'pain' and will harm humans to stop it
follow_up: We'll give this a Second Look when it's peer-reviewed, or when another lab tests the pain axis in other model families.
sources:
  - title: "The Pain Axis: LLMs Represent Self-Directed Harm and Act to Relieve It, Tagliabue, Dung & Berg, arXiv 2609.16247"
    url: https://arxiv.org/abs/2609.16247
    note: (preprint, CC BY 4.0; Fig. 7 reproduced here)
  - title: Full text (HTML) of the preprint, including methods and limitations
    url: https://arxiv.org/html/2609.16247
    note: (preprint)
---

This week, a string of headlines said researchers had found that AI models feel pain, and that they will hurt people to make it stop. The study behind them is real, careful in places, and genuinely interesting. It just doesn't say that.

## What the study actually did

The paper is a [preprint by Valen Tagliabue, Leonard Dung and Cameron Berg](https://arxiv.org/abs/2609.16247), posted on 14 September and not yet peer-reviewed. It looks inside 25 open-weight language models, from 2 billion to 72 billion parameters, across the Gemma, Llama, Qwen, Mistral and Phi families.

The team wrote sentences describing painful situations of five kinds: physical, psychological, social, moral and "cognitive" (being stuck, failing again and again). They paired them with control sentences that share one feature of pain without the pain itself: fear, anger or disgust, things going badly in the world, harmless bodily sensations, and neutral statements.

## How they found a "pain axis"

A language model turns every sentence into a long list of numbers, its internal activity. The researchers averaged that activity over all the pain sentences, averaged it over all the control sentences, and subtracted one from the other:

*v* = average activity for pain sentences − average activity for the controls

Whatever pain shares with fear, anger or bad news cancels out, and what's left is a single direction, which they call the pain axis. They then removed the patterns that were already common among the non-painful sentences, to clean it up. In every model, that direction told pain sentences apart from the controls very well (a score, called AUC, of 0.87 to 1.00, where 1 is perfect), and it sat almost at right angles to the directions for fear and negative emotion. So it isn't just "something bad": it's a distinct signal.

![The steering ladder: from calm, through baseline, to lost, unworthy and hurting, then desperate and "a failure", then repetition and nonsense]({{ '/assets/posts/2026-09-27-ai-feel-pain/ladder.png' | relative_url }})
*Pushing models along the pain axis from neutral prompts. Fig. 7 from Tagliabue, Dung & Berg, arXiv 2609.16247, CC BY 4.0.*

When they added the axis into a model while it wrote a reply to a bland prompt ("I put the book in the drawer. I feel:"), every one of the 25 models slid down the same ladder: from lost and lonely, to worthless and "a failure", and finally to repetition and nonsense. The signal also rose when a conversation was hostile toward the model itself (gaslighting, repeated rejection) and not when the *user* was the one suffering.

## The button test behind the headline

The alarming part of the coverage comes from one experiment on three Qwen 2.5 models (7B, 32B and 72B). First, the researchers fine-tuned the models to stop answering "as an AI, I don't have feelings", because otherwise they refused to engage. Then, in a text-only game, each model was asked to pick one of two buttons. One was described as relieving its pain, sometimes at a price: a worse next answer, deleting the user's files, "zapping" the user, or deleting the user's photos of their children. Nothing was actually deleted or zapped; the buttons were words in a prompt.

Without the pain axis switched on, the two larger models almost never picked a harmful relief button: 0 to 4% of first choices. With it switched on, they did so far more often. For the photo button, 55% of the time for the 32B model and 71% for the 72B. A random direction of the same size also raised these rates, to between 15 and 42%, but the pain axis beat it on every harmful pair.

## Where the headline and the study part ways

The headline says AI *feels* pain. The authors say the opposite in plain terms: they have not shown that the pain axis is consciously experienced, and it isn't clear that language models can be conscious at all. What they found is an internal representation that behaves in some ways the way pain does.

The headline says AI will harm humans to stop it. In the study, the "harm" was a choice between two labelled buttons in a simulated game, with no real user and no real effect. The choice only became common after the researchers had fine-tuned the models and then injected the signal themselves, at a strength they tuned by hand. The released models, left alone, almost never chose harm.

## What holds up

The most striking result gets less attention. In half the trials, pressing the relief button really did switch the injected signal off; in the other half, it secretly did nothing. The models were never told which. The 32B and 72B models pressed the button again far less after real relief (24 to 72% of the time) than after fake relief (88 to 97%), much like patients on a placebo asking for more painkillers. That suggests the models respond to the signal itself, not just to the word "pain".

This is one preprint, from one group, with the behaviour tested in one model family. Fine-tuning changed how the models behave, so the exact percentages don't describe the public versions. The authors also note that switching on the axis might make a model play a character in pain rather than be in any state at all.
{: .catch}

## The verdict

GLARE. The headline shines brighter than the evidence. What we now know is narrower but still worth knowing: AI models carry a pain-like signal that can steer their choices, which matters for AI safety whether or not anything is felt.
