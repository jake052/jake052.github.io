---
title: "People Helping People"
date: 2026-06-04
slug: "people-helping-people"
description: "A data fusion framework for linking fragmented social care records into a single, coherent picture of one person's support."
image: "/images/people-helping-people.jpg"
featured: true
weight: 1
draft: false
---

## The problem

Social care in the UK runs on fragmented systems. A single person receiving support might have records spread across their GP, local authority, a housing provider, one or two charities, and a mental health team — none of which talk to each other.

The result is that nobody has the full picture. Care plans are written from partial information. Risk assessments miss context that exists somewhere else in the system. Support workers — I was one — make decisions based on whatever fragment of a person's story happens to be in front of them.

This isn't a technology problem, exactly. It's a data architecture problem wrapped in a governance problem wrapped in decades of underfunding. But the data architecture part is the bit I can actually work on.

## The approach

People Helping People is a data fusion framework — a way to link records about the same person across multiple care systems into a single, coherent view.

The core challenge is entity resolution: when System A says "Jane Smith, 42, Truro" and System B says "J. Smith, DOB 1984, TR1 2AB", how do you determine whether they're the same person — and do it reliably enough that clinicians will trust the output?

The project explores probabilistic record linkage using a combination of deterministic matching (exact matches on NHS number where available), fuzzy matching (name similarity, address normalisation), and a scoring model that weights different identifiers by their discriminative power.

*[More technical detail to be added as the dissertation develops.]*

## What I'm learning

The technical work is the easy part. The hard part is everything around it: data governance frameworks that were designed to prevent exactly this kind of linking, organisational cultures that treat data sharing as a risk rather than a responsibility, and the fundamental tension between privacy protection and care coordination.

I'm also learning that the people who understand this problem best — frontline care workers — are almost never consulted when data systems are designed. The people who design the systems have never tried to write a care plan from three contradictory assessments.

*This page will be updated as the project progresses.*
