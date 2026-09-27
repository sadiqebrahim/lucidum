---
date: 2026-09-27 14:20:43 +0530
title: One laptop chip could fix quantum errors in real time
dek: In a simulation, IonQ researchers ran the error-correction decoder for up to 408 protected qubits on a single 12-core laptop chip, adding under 0.3% to run time at low error rates.
topic: Quantum computing
format: news
review_status: preprint
thumb: /assets/posts/2026-09-27-ionq-realtime-decoder/thumb.jpg
follow_up: We'll give this a Second Look when the decoder runs alongside real quantum hardware, or once the paper is peer-reviewed.
sources:
  - title: "Real-time decoder for a MegaQuOp quantum computer using a single CPU, Ye, Maksymov & Delfosse (IonQ), arXiv 2608.25027"
    url: https://arxiv.org/abs/2608.25027
    note: (preprint, CC BY 4.0; Fig. 1d reproduced here)
  - title: Full text (HTML) of the preprint, including methods and benchmark tables
    url: https://arxiv.org/html/2608.25027
    note: (preprint)
  - title: "Gold ion trap photo (illustrative), NIST, via Wikimedia Commons"
    url: https://commons.wikimedia.org/wiki/File:Gold_Ion_Trap_(6029437325).jpg
    note: (public domain)
---

Quantum computers make mistakes constantly, and something has to clean them up while the program is still running. A new preprint from three researchers at IonQ says that job, for a machine with a few hundred protected qubits, could be done by <mark>one ordinary laptop chip</mark>. The catch is in the setup: everything, including the quantum computer, was simulated.

## Why quantum computers need a fast helper

Qubits are fragile. Heat, stray fields and imperfect control flip them, so a working quantum computer spreads each useful "logical" qubit across many physical ones and keeps checking them. Those checks produce a steady stream of clues. An ordinary computer, called the decoder, reads the clues, works out which errors most likely happened, and tells the machine how to correct for them.

The decoder has to keep up. The paper puts it plainly: if the clues arrive faster than they can be processed, a backlog builds, and in the worst case the whole computation slows down dramatically. It also matters for a subtler reason. Many quantum programs make a measurement and then choose the next step based on the result, so the machine literally cannot move on until the decoder has an answer.

## What they did

[Min Ye, Andrii Maksymov and Nicolas Delfosse](https://arxiv.org/abs/2608.25027) built a full decoding pipeline for IonQ's proposed trapped-ion design, which they call the walking-cat architecture. They then tested it on three large programs, compiled all the way down to that design: a physics experiment on 102 logical qubits with more than a million of the most expensive kind of quantum step (T gates), and two simulations of magnetic materials, on 102 and 408 logical qubits. The biggest used 68 memory blocks and 20 "magic state" factories, built from 11,680 physical qubits.

All the decoding ran on a single 2024 Apple M4 Max chip in a MacBook Pro, using 12 of its 16 cores: eight for the main error decoder and four for a faster one that only handles measurements. The quantum computer and its errors were simulated, with error rates between 1 and 5 per 10,000 two-qubit operations, and each correction cycle assumed to take 1 millisecond (the two 102-qubit programs) or 5 milliseconds (the 408-qubit one).

## How they measured "keeping up"

The paper's scorecard is a single ratio it calls stretch: the number of extra pause cycles the machine had to insert while waiting for the decoder, divided by the number of cycles the program needs anyway. A stretch of 0.3% means a 1,000-cycle program takes about 1,003.

![Stretch against physical error rate for the three test programs, on a log scale]({{ '/assets/posts/2026-09-27-ionq-realtime-decoder/fig1d.png' | relative_url }})
*Fig. 1d from Ye, Maksymov & Delfosse (cropped), CC BY 4.0. Each line is one test program; lower is better.*

At an error rate of 1 in 10,000, stretch stayed under 0.3% for all three programs. At 5 in 10,000 it rose to under 12%. The 408-qubit program did best, at under 1% even at the highest error rate, because its slower 5-millisecond cycles gave the chip more time per step.

## The trick that made it fit on one chip

Measurements in this design add new kinds of error, which would normally force the decoder to rebuild its internal map of "which error sets off which alarm" every time a measurement starts or stops. That rebuilding is slow.

The authors noticed that each new error from a measurement sets off exactly the same alarms as an error that already exists in the normal checking cycle. So instead of adding a new entry, they merge the pair into one and update its probability: the chance that exactly one of the two happened, p_comb = p₁(1 − p₂) + p₂(1 − p₁). The map itself never changes, only a few numbers on it. They also cut the decoder's memory use by more than ten times, so a dozen copies could run side by side without choking the chip.

## Why it matters

Much of the work on fast decoders has gone into special hardware, such as FPGAs, GPUs and custom chips, because superconducting quantum computers need answers within microseconds. Trapped-ion machines run far slower, and this paper argues that for them, decoding at the scale of millions of operations need not be a bottleneck at all. The authors suggest a simple rule for scaling up: add CPU cores in step with the number of code blocks.

## The catch

This is a preprint from IonQ's own team, and it has not been peer-reviewed. No quantum computer was involved: the qubits, the errors and the programs were all simulated, and the timing depends on assuming 1 to 5 millisecond cycles and error rates that so far have been reached only on small trapped-ion devices. The authors also note that rare decoding failures, which would force a restart, are counted separately from stretch. The result says little about faster superconducting machines, which need answers a thousand times sooner.
{: .catch}

If real hardware behaves like the simulation, one of the classical chores of quantum error correction may turn out to be the easy part, at least for slow, steady trapped-ion machines.
