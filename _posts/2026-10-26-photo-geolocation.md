---
date: 2026-10-26 14:30:00 +0530
title: No GPS, and AI still finds where your photo was taken
dek: Reasoning AI models placed about one in four ordinary photos within a kilometre, with no landmarks or location data. The giveaway is the small stuff, and that is also the fix.
topic: AI
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-26-photo-geolocation/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "Not Where You Think: Protecting Location Privacy Against Reasoning-Based Geolocation, Shi, Xiao, Li, Chang, Vorobeychik, Jacobs, Patwari and Zhang, arXiv 2610.30439 (Oct 2026)"
    url: https://arxiv.org/abs/2610.30439
    note: (preprint, CC BY 4.0)
---

Turning off location tagging before you post a photo feels like enough. A [new study](https://arxiv.org/abs/2610.30439) suggests it isn't. AI models that reason step by step about a picture can often work out where it was taken from the scene alone, sometimes down to the street.

## The test

The researchers built GeoTrace, a structured reasoning attack that has a multimodal AI model look at a photo, reason about what it sees and commit to a location. They ran it on 525 ordinary photos from around the world. These weren't tourist shots: none had landmarks, and none carried location metadata.

## How close it got

With Gemini-3-Flash, GeoTrace placed <mark>25.71% of the photos within one kilometre</mark> of where they were taken. With GPT-5-mini, the figure was 16.95%. That's roughly one photo in four, and one in six, located to street level from pixels alone.

## The giveaway is the small stuff

The team then looked at what the models were relying on. Broad properties of a scene, such as the landscape, the vegetation or the light, mostly narrow things down to a region. Precise guesses depended on small, distinctive details: think of the style of a kerb, the colour of a road sign or a particular plant (those examples are ours). Crucially, those details are few, and they can be edited.

## A defence: GeoShift

That finding suggested a fix. GeoShift picks a plausible false location and rewrites only the high-impact clues so the photo points there instead. The rest of the image is left alone.

![Bar chart: street-level hits fall to 3.8% for Gemini-3-Flash and 2.5% for GPT-5-mini; a drawn street photo before and after looks the same.]({{ '/assets/posts/2026-10-26-photo-geolocation/geoshift.png' | relative_url }})
*After GeoShift, street-level hits collapse while the photo looks the same (the street scene is our drawing).*

With GeoShift applied, street-level accuracy fell from 16.95% to 2.48% for GPT-5-mini and from 25.71% to 3.81% for Gemini-3-Flash. The authors report that visual quality was preserved and that the defence held up against adaptive attacks, where the attacker knows a defence may be in use.

## The catch

This is a preprint and hasn't been peer reviewed. The results come from 525 photos and two models; other models, or photos with landmarks, could behave differently. GeoShift is a research method, not a feature in any app you can switch on today.
{: .catch}

Stripping the GPS tag hides the coordinates, not the small details that give the street away.
