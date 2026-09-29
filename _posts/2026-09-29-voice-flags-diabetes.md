---
date: 2026-09-29 10:26:50 +0530
title: 20 seconds of your voice could flag diabetes
dek: An AI listening to 20-second recordings of people reading a fable ranked those with type 2 diabetes above those without 80% of the time in 7,319 UK adults, though it also flagged nearly half of people without the disease; the results are a conference presentation, not yet peer-reviewed.
topic: Health
format: explainer
review_status: preprint
thumb: /assets/posts/2026-09-29-voice-flags-diabetes/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed and tested in clinics.
sources:
  - title: Signs of type 2 diabetes detected in 20 seconds of speech by AI-based model, Medical Xpress (EASD 2026 presentation, thymia and RMIT University)
    url: https://medicalxpress.com/news/2026-09-seconds-speech-diabetes-ai-based.html
    note: (conference abstract, not peer-reviewed)
  - title: The Hare and the Tortoise, Arthur Rackham (1912), Wikimedia Commons (public domain; cover and thumbnail)
    url: https://commons.wikimedia.org/wiki/File:Tortoise_and_hare_rackham.jpg
---

Read one of Aesop's fables aloud for 20 seconds, and an AI model can often tell whether you have type 2 diabetes. In a test on recordings from 7,319 adults in the UK, it put the person with diabetes ahead of the person without it in 80% of pairs, according to research presented this week at the European Association for the Study of Diabetes meeting in Milan, [as reported by Medical Xpress](https://medicalxpress.com/news/2026-09-seconds-speech-diabetes-ai-based.html).

## Why anyone would screen by voice

Type 2 diabetes is common, and catching it early matters, because years of high blood sugar lead to heart disease and nerve damage. Yet in the UK roughly 30% of people with it haven't been diagnosed. The NHS offers a health check every five years to people aged 40 and over, which includes a diabetes test, but the study's authors say only about 40% of the people eligible actually go. Something that works over the phone could reach the people who never make that appointment.

## What they did

Earlier studies had linked type 2 diabetes to subtle changes in how people speak: a voice that is hoarser and rougher, with less control of breath. A team at the company thymia, led by Roseline Polle and Elisa Brann, worked with RMIT University in Melbourne to train an AI model to pick up those changes. It learned from 63,283 voice samples from 21,129 people in the UK and US, each of whom had said whether they'd been diagnosed with diabetes.

The model was then tested on something new: remote 20-second recordings of people reading an Aesop fable. In the first test, 7,319 UK adults took part, and 217 of them reported having type 2 diabetes. In the second, 801 of them also took an HbA1c blood test at home within three months of their recording. HbA1c measures average blood sugar over the previous two to three months and is the standard test for diagnosing the disease.

## How to read the numbers

The headline figure is a ranking score. Take any one person with diabetes and any one person without it. The question is how often the model gives the higher risk score to the person with diabetes. Pure guessing would be right half the time; this model was right <mark>80% of the time</mark> against what people reported, and 75% of the time against the blood tests.

The blood-test group also shows the trade-off any screening tool has to make. The model caught 82% of the people whose blood test showed diabetes, which is its sensitivity. But its false-positive rate was 47%: it also flagged nearly half of the people who didn't have diabetes. It did sort people into low, medium and high risk, and none of the people it put in the low-risk group had blood results in the diabetic or prediabetic range.

![Two grids of 100 dots: in the left grid, 82 dots are lit for people with diabetes the model caught; in the right grid, 47 dots are lit for people without diabetes it flagged.]({{ '/assets/posts/2026-09-29-voice-flags-diabetes/diagram.png' | relative_url }})
*Out of every 100 people with diabetes, it caught 82. Out of every 100 without it, it raised 47 false alarms.*

## Why it matters

With that many false alarms, the model can't diagnose anyone, and the researchers don't claim it can. What they propose is triage: a quick recording, made by phone or in an app, that helps a doctor decide who should get a blood test first. Because it's cheap and remote, it could reach people who never come in for a check. The researchers say it would sit alongside blood testing, not replace it.

## The catch

These results come from a conference presentation, not a peer-reviewed paper, and the tool hasn't yet been tested in a clinic. Most people's diabetes status was self-reported, and only 801 had a blood test. The model worked less well for Black participants, which the authors put down to how few Black participants with diabetes were in the data, and for people with heart disease, high blood pressure or obesity, conditions that often come with diabetes and may change the voice in similar ways. A 47% false-positive rate would also send many healthy people for blood tests.
{: .catch}

A 20-second voice recording could become a first filter for who needs a blood test, but for now, the blood test is still the only way to know.
