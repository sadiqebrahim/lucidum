---
date: 2026-10-05 23:53:00 +0530
title: Archimedes' sphere trick, proved one of a kind
dek: Archimedes showed that a slice of a sphere between two parallel planes always has area 2πh. A new proof shows that only the sphere can do this, even for a single fixed width.
topic: Mathematics
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-05-archimedes-sphere/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "The sphere is the only closed surface satisfying the fixed-width Archimedean property, Mijia Lai, arXiv 2610.01550 (1 Oct 2026)"
    url: https://arxiv.org/abs/2610.01550
    note: (preprint)
---

Slice a ball into rings of equal thickness, and every ring has exactly the same surface area. Archimedes knew this more than 2,000 years ago. A [new proof](https://arxiv.org/abs/2610.01550) by Mijia Lai shows that <mark>no other closed surface can do it</mark>.

## Archimedes' 2πh

Take a sphere of radius 1 and cut it with two parallel planes a distance h apart, both meeting the sphere. The band between them always has area 2πh, wherever you make the cut.

![A unit sphere with a band between two planes a distance h apart; the band's area is 2πh.]({{ '/assets/posts/2026-10-05-archimedes-sphere/band.png' | relative_url }})
*Area of band = 2πh.*

## Why it works

Near the top of the sphere the band is a small circle, but the surface there is steep, so the band is wider along the surface than its height suggests. Near the middle the circle is large, but the surface is almost vertical. The two effects cancel exactly: circumference times slant is the same at every height.

![A narrow, steep band near the top and a wide, flat band at the middle; circumference times slant is the same.]({{ '/assets/posts/2026-10-05-archimedes-sphere/cancel.png' | relative_url }})
*The cancellation behind the rule.*

## The new proof: only the sphere

Could some other shape share the property? Lai proves the answer is no: among connected, smooth, closed surfaces sitting in ordinary 3D space, having the 2πh property for just one fixed width h is enough to force the surface to be the unit sphere.

As background, not part of the new proof: the same idea underlies Lambert's equal-area cylindrical map, which wraps the globe onto a cylinder and keeps areas true.

## Why it matters

Results like this, that a single simple property pins down one shape, are how mathematicians understand what makes a shape special. Archimedes' observation turns out to be not just a curiosity but a defining fingerprint of the sphere.

This is a preprint and hasn't been peer-reviewed. The result covers smooth, closed, connected surfaces in ordinary space; surfaces with edges or corners aren't covered.
{: .catch}

Archimedes' slicing trick is a fingerprint: only the sphere has it.
