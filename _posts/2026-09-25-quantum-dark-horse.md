---
title: Particles nature never made just went universal
dek: On a 54-qubit trapped-ion machine, physicists braided and fused made-to-order particles to get every operation a quantum computer needs, in a proof-of-principle experiment.
topic: Quantum computing
format: explainer
review_status: peer-reviewed
thumb: /assets/posts/2026-09-25-quantum-dark-horse/thumb.jpg
sources:
  - title: Universal gates from braiding and fusing anyons on quantum hardware, Lo, Lyons et al., Nature (2026)
    url: https://doi.org/10.1038/s41586-026-10709-y
  - title: Quantum computing's "dark horse" just proved it can go universal, ScienceDaily
    url: https://www.sciencedaily.com/releases/2026/09/260924020403.htm
    note: (university news, University of Chicago)
  - title: Planar ion trap, NIST, Wikimedia Commons (public domain; shown in the Reel as an illustrative ion-trap chip)
    url: https://commons.wikimedia.org/wiki/File:Planar_Ion_Trap_(5941086002).jpg
---

A team of physicists has built particles that don't exist on their own anywhere in nature, inside a quantum computer, and shown that moving them around and merging them is enough to carry out any quantum computation. The experiment used 54 qubits on one trapped-ion machine, and it was a test of the building blocks, not a working computer. But it is the first time this route has been shown to be complete.

## What they did

The work, [published in Nature](https://doi.org/10.1038/s41586-026-10709-y), comes from researchers at the University of Chicago, Harvard, Stony Brook University and the company Quantinuum. They ran it on Quantinuum's H2 processor, where each qubit is a single ion held in place by electric fields.

The team entangled 54 of those qubits into one collective state. Seen as a whole, that state behaves as if it contained a new kind of particle, called a **non-Abelian anyon**. These particles exist only as patterns in the entangled qubits; one of the researchers, Ruben Verresen, [compares it](https://www.sciencedaily.com/releases/2026/09/260924020403.htm) to building a small alternative universe with its own rules.

The particular anyons they made follow the symmetries of an equilateral triangle: the ways you can rotate or flip one so it looks the same. Pairs of them were used to store "qutrits", units of quantum information with three levels instead of a qubit's two.

## How it works

Anyons store information in their history. Each one carries an internal state that changes when it is moved around another, a move called **braiding**, and for non-Abelian anyons the order of the moves matters.

A braid of hair works the same way. With three strands, crossing the left pair and then the right pair gives a different braid from crossing the right pair first. And a small tug on the strands doesn't turn one braid into the other. That second property is the attraction: because the information is spread across many entangled qubits rather than sitting in one place, it is naturally shielded from some of the small disturbances that knock ordinary qubits off course.

![Two three-strand braids side by side: crossing the left pair then the right pair ends with the highlighted strand on the right; crossing them in the other order ends with it in the middle.]({{ '/assets/posts/2026-09-25-quantum-dark-horse/diagram.png' | relative_url }})
*Same three strands, same two crossings, different order: the highlighted strand ends up in a different place.*

Braiding alone was not enough, though. In 2024 a team including Verresen made a different set of anyons, based on the symmetries of a square, on the same kind of hardware, but braiding them could not perform every operation a quantum computer needs. The missing piece in the new work is **fusion**: bringing two anyons together and measuring what they combine into. The team showed one entangling gate made by braiding and two measurements made by fusion, which together make up a [universal gate set](https://www.sciencedaily.com/releases/2026/09/260924020403.htm). The idea was proposed in theory in 2003 by Carlos Mochon, then a student of John Preskill at Caltech.

## Why it matters

Quantum computers make errors constantly, so serious designs protect their information by spreading it over many physical qubits. The catch with most of those schemes is that the protected information can't be pushed through every kind of operation directly. To fill the gap, engineers prepare special resources called "magic states", which are usually made by a clean-up process called distillation that can use up a large share of a machine's qubits.

In this experiment the anyons produced a magic state directly, using only topological moves. Henrik Dreyer of Quantinuum, a co-author, calls these codes a <mark>dark horse</mark> in the race to error-corrected quantum computing: if the approach scales, it could skip what is usually the most expensive step.

## The catch

This was a proof of principle. The experiment did not run active error correction; it tested each building block on its own and checked that the magic state came out as theory predicts. Joining these operations to working error correction is the next hurdle, and until that is done nobody knows how well the advantages survive at scale. The machine that runs a useful computation this way does not exist yet.
{: .catch}

## What to watch

The next result worth waiting for is the same braids and fusions running with error correction switched on.
