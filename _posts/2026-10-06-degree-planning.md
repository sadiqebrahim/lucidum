---
date: 2026-10-06 11:50:00 +0530
title: Planning your degree is a hard maths problem
dek: Choosing courses so you graduate as fast as possible is easy for a computer, until each term gets a credit cap. Then it becomes one of computing's hardest kinds of puzzle.
topic: Computing
format: explainer
review_status: preprint
thumb: /assets/posts/2026-10-06-degree-planning/thumb.jpg
follow_up: We'll give this a Second Look when it's peer-reviewed.
sources:
  - title: "The Plan Language of a Curriculum: A Formal Model and the Complexity of Degree Planning, S. Turaev, M. John and M. Awad, arXiv 2610.03392 (2 Oct 2026)"
    url: https://arxiv.org/abs/2610.03392
    note: (preprint)
---

Every student has done it: lay out the courses, check the prerequisites, and try to fit everything in before graduation. It feels like a scheduling chore. A [new paper](https://arxiv.org/abs/2610.03392) shows that, mathematically, it can be one of the hardest kinds of problem in computing, and pins down exactly what makes it hard.

## A degree as a puzzle

Sherzod Turaev, Mary John and Mamoun Awad model a curriculum as rules that generate every possible study plan. Prerequisites are logical conditions, which can include either-or options ("course A or course B first"). Degree requirements say you need enough credits in each area. And a plan is a sequence of terms, each with a maximum number of credits.

They then ask about the two natural goals: finishing in the fewest terms, and finishing with the fewest total credits.

## Fastest route: easy, until the cap

With no limit on credits per term, finding the fastest route to graduation is efficient for a computer, even with either-or prerequisites and any number of electives. The either-or logic never makes this goal harder.

But as soon as the per-term credit cap actually binds, the problem becomes <mark>strongly NP-hard</mark>, even with no prerequisites at all. Deciding what goes in each term becomes a packing problem, with no known method that solves every case quickly.

![Three terms with a credit cap; courses must be packed into them like boxes.]({{ '/assets/posts/2026-10-06-degree-planning/credit-cap.png' | relative_url }})
*With a credit cap, filling terms becomes a packing puzzle.*

## Fewest credits: the opposite story

The second goal behaves the other way round. Either-or prerequisites and overlapping electives each make the fewest-credits problem strongly NP-hard on their own, and the cap doesn't matter. With only plain "and" prerequisites and mandatory courses, it's efficient. So the two goals are hard for completely different reasons.

The paper also shows that a widely used measure of curricular complexity, its delay factor, gives an upper bound on time to degree that's exact for simple prerequisites and can be loose otherwise.

## Real universities

The authors applied the model to curricula from 22 universities. They found that 88% of courses with prerequisites use only plain "and" conditions, and that in practice the credit cap, not the prerequisite logic, is what limits time to degree. The data set is openly available.

## The catch

This is a preprint and hasn't been peer reviewed. "NP-hard" describes the worst cases; real timetables can often still be solved quickly in practice. The result is about planning, not about how hard any particular degree is.
{: .catch}

The credit cap per term is what turns planning a degree into a hard puzzle.
