---
title: "People Helping People"
date: 2026-06-12
slug: "people-helping-people"
description: "A data fusion layer for social care — turning the fragments scattered across notes, records, and conversations into a single, living picture of one person."
featured: true
status: "In progress"
image: "/images/projects/php-living-plan.png"
weight: 1
draft: false
---

*The venture · In active development*

Think about your own support plan — the document someone would have to write if a stranger had to support you tomorrow. How you communicate. The shifts in your tone when you're tired. Your morning routine, in order, including the small stuff that makes you, you.

It's really hard to write down. And in social care, nobody is ever working from the full version. A person's reality is scattered across daily notes, risk assessments, incident reports, a support plan written eighteen months ago, and something a family member said last Tuesday. Each fragment sits in a different place. Nobody joins them up — and the person in the middle, who often can't fill that gap themselves, is the one who pays for it.

I spent eight years inside this problem — as a support worker, then managing supported living services. It's also personal: my brother Ollie is supported by this system. For people like him, the difference between fragmented data and fused understanding is the difference between reactive support and care that actually knows who he is.

## The idea

Military intelligence solved this problem decades ago. Satellites, drones, ground patrols — each one a fragment, individually just noise. Fused together, they become a common operating picture: one living model of what's actually happening. Hall and Llinas called it data fusion, and it's now standard in defence, autonomous vehicles, and fraud detection.

Nobody has applied it to social care. People Helping People is that layer: every source feeding one structured, continuously updated model of the person — same person, same data, different lens for the support worker planning a shift, the social worker reviewing care, the family member wanting to know how this week went.

Under the hood, that means confidence weighting (how sure are we about each data point, and does newer evidence outweigh older?), an event-driven design that reacts when new information arrives rather than waiting for a review date, language models that work with meaning rather than keywords, and agentic loops that can notice a contradiction and ask a human to resolve it rather than guessing.

## Why nobody's building it

Adult social care in England spends around £30bn a year. Eighty per cent of providers are now on digital records — the data is being captured. But every care-tech competitor is fighting over the output layer: better forms, nicer dashboards, prettier documents. Of the twenty-seven council technology strategies I analysed, only five even mention AI.

The layer underneath — the data architecture that would make every output better — is empty. Kim and Mauborgne would call it a blue ocean. I'd put it more simply: I'm not avoiding competition, I'm competing on a different axis.

## Where it actually is

Honestly: architectural design and MVP prototyping. The [social story builder](/projects/social-story-builder/) proved the output layer was crowded; the [care plan update system](/projects/care-plan-update-system/) proved fusion produces a better picture than any single source — and is the first working piece of the platform. Every MVP cycle tests the core hypothesis on synthetic data before any real record goes near it.

{{< figure src="/images/projects/php-living-plan.png" alt="The PHP prototype refreshing a care plan marked stale at 14 months, reading every shift note written since" caption="A plan that was 14 months stale, refreshed from every note written since" >}}

The open questions are real too. Will anyone pay, and how much? And the one that matters most: this is AI mediating the voice of people who often can't verify what's written about them. Decisions get made on this data. Building the ethics in — co-produced with the people the system describes — isn't a compliance step. It's the product.

{{< annotation >}}Every person deserves to be known by the people who support them.{{< /annotation >}}
