---
title: "Care Plan Update System"
date: 2026-05-01
slug: "care-plan-update-system"
description: "An agentic prototype that reads daily care notes, spots what's changed, and proposes care plan updates with an evidence trail — the second PHP hypothesis."
status: "Complete"
image: "/images/projects/care-plan-evidence.png"
weight: 3
draft: false
---

*The second People Helping People hypothesis · Spring 2026*

Care plans decay the moment they're written. The real, current knowledge about a person lives in daily notes, handover conversations, and staff memory — and none of it feeds back into the plan.

Here's what that looks like in practice. The care note says: *"Had a good day. Settled well at bedtime. No concerns."* The worker who wrote it spent eight hours with that person. They knew she was restless after tea, pacing the corridor. They tried the weighted blanket — no change. They put on the playlist she made with her sister, and she settled by nine. Third evening that week. None of that made it onto the page, and what did make it onto the page never reached the plan.

This isn't carelessness. There's simply no mechanism to keep a plan alive — so the plan says one thing, the notes tell a different story, and nobody joins them up. Then a worker leaves (24% of the workforce does every year; 39% in their first year) and what they knew leaves with them. Across four years of Safeguarding Adult Reviews in England — 652 of them — reviewers found poor information-sharing in three quarters of cases. The knowledge existed somewhere. It just never reached the people who needed it.

{{< annotation >}}It's half ten at night and a registered manager somewhere is rewriting a care plan by hand, because nothing connects the notes back to it.{{< /annotation >}}

## What I built

An agentic system that does the joining up. It reads daily care notes against the existing support plan, identifies meaningful changes — what worked, what didn't, what contradicts the plan as written — and proposes updates, each with an evidence trail back to the notes that justify it.

The manager stays in control. They review each suggestion, accept or reject it, and the plan ends up reflecting the person as they are now, not as they were eighteen months ago. Nothing changes without a human deciding it should. It's a working prototype, tested on synthetic data — no real service users' records — and you can [see it working](https://careplan.peoplehelpingpeople.co.uk).

{{< figure src="/images/projects/care-plan-evidence.png" alt="A care plan in the prototype where clicking any citation reveals the daily note that justifies the change" caption="Every change carries its evidence — live at careplan.peoplehelpingpeople.co.uk" >}}

## Why it mattered

The [first build](/projects/social-story-builder/) taught me the output layer was crowded. This one was closer to the real problem: it proved that AI can bridge the gap between operational recording — the daily grind of notes and handovers — and the strategic planning layer that's supposed to describe a person's support. Patterns a tired human skims past at the end of a long shift, the system surfaces: the third restless evening that week.

## And what it exposed

Even good care notes are one data source. A person's reality is also in their risk assessments, incident reports, health records, what a family member said last Tuesday. Make the notes richer and they still pile up in the same silo — I'd improved one fragment, and fragments are still fragments.

Real understanding of a person means fusing all of it. That's the problem [People Helping People](/projects/people-helping-people/) now exists to solve — and this prototype became its first working piece.
