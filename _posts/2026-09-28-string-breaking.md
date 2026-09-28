---
date: 2026-09-28 09:32:00 +0530
title: A quantum computer made matter pop into existence
dek: A Duke-led team used a chain of 13 trapped ions to simulate "string breaking", the moment a stretched string of force snaps and turns its energy into new particles.
topic: Quantum computing
format: explainer
review_status: peer-reviewed
thumb: /assets/posts/2026-09-28-string-breaking/thumb.jpg
sources:
  - title: "String-breaking dynamics in a quantum simulator, De, Lerose, Luo, Surace, Schuckert, Bennewitz et al., Nature Physics (2026)"
    url: https://doi.org/10.1038/s41567-026-03422-0
    note: (paper; details checked via Crossref, the Nature page itself was not reachable from our tools)
  - title: Quantum device simulates how matter forms when strings break, Phys.org
    url: https://phys.org/news/2026-09-quantum-device-simulates.html
    note: (Duke University news, via Phys.org)
---

Pull two quarks apart and something strange happens. The string of force between them doesn't weaken as it stretches. It stores more and more energy until it snaps, and where it breaks, <mark>brand-new particles appear</mark>. A team led by Duke University has now played this out on a quantum computer, a chain of 13 trapped ions, and watched the string break step by step. The work is published in [Nature Physics](https://doi.org/10.1038/s41567-026-03422-0).

## The string that won't let go

Quarks, the particles inside protons and neutrons, are never found on their own. They are held together by the strong force, which behaves like a string between them. Most forces fade with distance, like the electric pull between charges. This one doesn't: past a short range, the pull stays roughly the same however far you stretch it.

That has a simple consequence for energy. If the pull is constant, every extra bit of stretch adds the same amount of energy:

![The equation E equals sigma times r, and a graph where doubling the distance doubles the energy.]({{ '/assets/posts/2026-09-28-string-breaking/string-energy.png' | relative_url }})
*E = σr: the string's energy grows in a straight line with its length.*

Here σ is the string's tension, the energy it stores per metre, and r is how far apart the quarks are. Stretch it twice as far and it holds twice the energy.

## Energy becomes matter

Einstein's E = mc² says energy and mass are two forms of the same thing. Making a new particle and its antiparticle costs at least 2mc² of energy. So once the string holds more than that, it becomes cheaper for the string to break and spend its energy on a new pair: a particle at one new end, an antiparticle at the other. Instead of one long string, you get two short ones.

![A graph: the string's energy rises until it reaches the 2mc squared line, and below, the string snaps into two with a new particle and antiparticle at the break.]({{ '/assets/posts/2026-09-28-string-breaking/string-snap.png' | relative_url }})
*When the stored energy passes 2mc², the string breaks and a new pair appears.*

This is the textbook picture of "string breaking". It is hard to calculate for real quarks, because the particles, the string and the new pairs are all tangled together quantum-mechanically, and it plays out over time.

## What the team did

The researchers, led by Christopher Monroe's group at the Duke Quantum Center with the University of Maryland, Oxford, Caltech, Cornell and KU Leuven, built a simpler, one-dimensional version of this physics and [encoded it into a chain of 13 trapped ions](https://phys.org/news/2026-09-quantum-device-simulates.html): charged atoms held in a row by electric fields and steered with precisely controlled laser beams. Tracking how the system changed over time, they saw effective charges emerge and reconstructed how the string broke.

![A row of 13 ions; a string between two charges breaks in the middle and two new charges appear.]({{ '/assets/posts/2026-09-28-string-breaking/string-ions.png' | relative_url }})
*A schematic of the idea, not the team's exact encoding.*

At this size, ordinary computers can still simulate the same system, and the team checked its results against them. They agreed.

## Why a quantum computer

The reason to use one is scale. To follow a quantum system exactly, a normal computer has to keep track of a number of possibilities that doubles with every particle added: 2ⁿ for n ions. Thirteen ions means 8,192. Fifty means about a quadrillion. Bigger, more realistic versions of string breaking will need quantum machines, and they could help show how matter formed in the early universe, just after the Big Bang.

This is a simplified model, one-dimensional and much smaller than the physics of real quarks, and at 13 ions it doesn't yet do anything a classical computer can't. It's a demonstration of the method, not a new result about the strong force. Other groups, including teams using Google's and QuEra's hardware, have shown similar string breaking on different machines.
{: .catch}

A quantum computer can now watch energy turn into matter, one step at a time.
