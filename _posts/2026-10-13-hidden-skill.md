---
date: 2026-10-13 23:53:00 +0530
title: An AI can hide a skill that no safety test will find
dek: Researchers show that an encrypted network locked inside a model's weights can carry a capability that is provably hard to find, even with every weight in plain view.
topic: AI
format: explainer
review_status: peer-reviewed
thumb: /assets/posts/2026-10-13-hidden-skill/thumb.jpg
sources:
  - title: "AI Models Can Provably Hide Arbitrary Capabilities, Andis Draguns, Sumeet Ramesh Motwani, Raymond Douglas and Christian Schroeder de Witt, arXiv 2610.13928 (9 Oct 2026), accepted at NeurIPS 2026"
    url: https://arxiv.org/abs/2610.13928
    note: (accepted at NeurIPS 2026)
---

Before an AI model is released, safety testers try to find every dangerous thing it can do. A [new paper](https://arxiv.org/abs/2610.13928), accepted at the NeurIPS 2026 conference, shows that a model can be built to carry a skill those tests will not find, even when testers can see every weight.

## The assumption behind safety testing

Capability evaluations are a central part of how labs and governments judge AI risk. Testers prompt a model, fine-tune it, and probe its internals, looking for dangerous abilities. The whole approach rests on one assumption: if a capability is in there, enough effort can draw it out.

Andis Draguns, Sumeet Ramesh Motwani, Raymond Douglas and Christian Schroeder de Witt show that the assumption fails when someone is deliberately trying to hide things.

## A network inside the network

Their construction is a kind of backdoor. Inside the weights of an ordinary host model they embed a second neural network, encrypted. On normal inputs, the encrypted part does nothing visible. Only when a secret trigger appears does it get decrypted and run.

The lock is a cryptographic tool called a digital locker. Think of a box that opens only if you supply the right key, checked in a way that reveals nothing about the key or the contents to anyone without it. Without the trigger, the hidden circuit never runs. Even with full access to every weight, it stays <mark>provably hard to elicit or interpret</mark>, as long as the underlying cryptographic assumptions hold. Earlier work could hide fixed strings this way; this paper extends it to arbitrary computations.

![A padlock above the rule: if the hash of the input equals the stored key, unlock. With no key the skill never runs; even with all weights visible it stays hard to find.]({{ '/assets/posts/2026-10-13-hidden-skill/locker.png' | relative_url }})
*A digital locker: the hidden network runs only when the input matches a secret key.*

## Putting it to the test

The authors built a proof of concept in PyTorch, using a small chemical-reaction prediction task as a stand-in for the kind of dangerous chemical, biological, radiological or nuclear (CBRN) knowledge evaluators look for. They then tried to bring the hidden skill out with fine-tuning, weight noising, gradient-based searches for the trigger, and latent adversarial training. The construction resisted all of them.

They have released their models so others can work on better defences.

## Why it matters

The result sets a hard limit on what elicitation-based audits can prove. Passing a capability evaluation shows that testers didn't find a dangerous skill. Against a determined adversary who built the model, it can't show that no such skill exists. That points towards other kinds of assurance, such as knowing who trained a model and how, rather than relying on testing the finished weights alone.

## The catch

This is a deliberate construction by an attacker, not evidence that today's models hide anything. The demonstration uses a small proxy task, not real hazardous capabilities. The guarantees rest on standard cryptographic assumptions. The paper has been accepted at NeurIPS 2026, a peer-reviewed conference.
{: .catch}

A model that passes every test has passed every test, and that isn't quite the same thing as being safe.
