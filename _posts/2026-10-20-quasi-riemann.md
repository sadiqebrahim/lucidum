---
date: 2026-10-20 23:50:00 +0530
title: An AI proved the quasi-Riemann hypothesis. What does that mean?
dek: An OpenAI-generated proof fences every nontrivial zero of the zeta function into a narrower strip than anyone had managed. Experts largely think it's right, and that it's badly written.
topic: Maths
format: news
review_status: n/a
thumb: /assets/posts/2026-10-20-quasi-riemann/thumb.jpg
follow_up: We'll give this a Second Look once the proof has been through peer review or full human checking.
sources:
  - title: "AI Proved the Quasi-Riemann Hypothesis. What Happens Now?, Konstantin Kakaes, Quanta Magazine (19 Oct 2026)"
    url: https://www.quantamagazine.org/ai-proved-the-quasi-riemann-hypothesis-what-happens-now-20261019/
    note: (news; the proof is not peer reviewed)
---

Mathematicians have checked the first 12 trillion "nontrivial zeros" of the Riemann zeta function, and every one sits on the same line. That still isn't a proof. Now, [reports Quanta Magazine](https://www.quantamagazine.org/ai-proved-the-quasi-riemann-hypothesis-what-happens-now-20261019/), an AI-generated proof has shown that none of them can stray beyond a fence.

## The biggest open problem in maths

The Riemann hypothesis, posed in 1859 and open for over 160 years, is about where the zeta function equals zero. Bernhard Riemann showed that those zeros govern how the prime numbers thin out along the number line. The hypothesis says every nontrivial zero has a real part of exactly 1/2: they all lie on one vertical line.

Checking zeros one by one can never settle it. One stray zero anywhere would, in Enrico Bombieri's words quoted by Quanta, create havoc in the distribution of the primes.

## Narrowing the strip

Riemann proved that the nontrivial zeros lie in a vertical strip between 0 and 1. In 1896, showing that no zeros sit on the strip's edges gave the prime number theorem. The "quasi-Riemann hypothesis" asks for less than the full conjecture: prove that all the zeros lie inside some strictly narrower strip. The narrower it is, the more you can say about the primes.

## What OpenAI's proof claims

Among 377 results OpenAI announced on 6 October, one claimed to settle it. There are two versions. A 199-page paper, formally verified in the Lean proof language, puts every nontrivial zero between 1/8 and 7/8. A later 49-page paper, not yet formally verified, proves a slightly weaker strip, <mark>between 1/12 and 11/12</mark>. Mathematicians are mostly studying the shorter one.

![The zeros, known to lie between 0 and 1, are proved to lie between 1/12 and 11/12.]({{ '/assets/posts/2026-10-20-quasi-riemann/strip.png' | relative_url }})
*A narrower strip: every nontrivial zero lies strictly between 1/12 and 11/12.*

## What experts say

According to Quanta, the experts studying it largely agree the result is correct. Alexander Dunn calls it "a surprising synthesis of well-known ideas", and Maksym Radziwiłł says most consequences of the full hypothesis already follow from the quasi version. The proof relies on a family of functions built with metaplectic forms, and on a formula Dunn and Radziwiłł proved in 2021. Radziwiłł also describes both papers as horribly written by journal standards.

## The catch

The proof hasn't been peer reviewed, and the 49-page version isn't formally verified. Peter Sarnak says he won't call it a theorem until humans have checked and understood every detail. And this is not the Riemann hypothesis itself: several mathematicians doubt these methods can reach the line at 1/2.
{: .catch}

AI didn't solve the Riemann hypothesis, but it seems to have built a fence around the zeros that nobody had managed before.
