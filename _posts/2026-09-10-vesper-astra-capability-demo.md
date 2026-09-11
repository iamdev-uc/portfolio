---
layout: post
title: "VESPER: using a space sandbox as an Astra capability demo"
date: 2026-09-10 09:00:00 +0200
last_modified_at: 2026-09-11 09:00:00 +0200
description: >
  Why a small 3D space game is a better AI capability demo than another generated landing page: it forces one workflow across frontend, simulation, networking, packaging, docs, and tests.
tags: [ai, projects, gpt]
---

A generated landing page can look impressive and still tell you almost nothing about whether an AI system can carry a software project across boundaries. **VESPER** is more interesting precisely because it is awkward: real-time graphics, game rules, state, networking, persistence, packaging, and tests all have to agree.

I use the project as an **Astra capability demo**. Not because “AI can make games” is a useful conclusion, but because a self-contained game prototype is a good stress test for end-to-end software work.

## The demo constraint

The goal was deliberately practical: a small space sandbox that could be opened locally for solo play, while still including a server path for a handful of friends.

The resulting package has four planets, procedural ships, pirates, a modular hangar, economy, weapons and damage systems, optional PvP, and a WebSocket multiplayer server. Solo mode works from static files; the networked version can run with Node.js or Docker.

That breadth is exactly what makes it useful as an AI evaluation artifact. A model can be brilliant at one file and still lose the plot when state has to stay consistent across ten of them.

## What Astra-style assistance changes

The meaningful shift with systems like GPT‑6 Astra is not “better autocomplete.” It is the ability to keep a larger goal active while moving through implementation steps: inspect files, edit multiple components, run tests, read failures, revise, document, and package.

That creates a different development loop:

1. Define the product boundary and the non-negotiable constraints.
2. Let the model implement a coherent slice across files.
3. Run the real checks, not a prose self-review.
4. Use failures to tighten both code and specification.
5. Repeat until the artifact is runnable by someone who did not participate in the conversation.

The final step matters. “Works in the chat” is not a product property.

## Verification is the real capability test

VESPER includes 18 rule-level tests and one live HTTP/WebSocket integration test using eight clients. They cover movement, fuel, landing, economy, equipment, projectiles, damage, hostile inputs, room access, capacity, shared state, and persistence after restart.

That does not prove the game is production-ready. It proves something more useful for a portfolio demo: the prototype has **executable expectations**.

<div class="callout callout--accent">
The strongest AI-assisted workflow I have found is not “prompt → code.” It is “intent → artifact → test → correction → documented artifact.” The model is valuable because it can move quickly around that loop without losing the original objective.
</div>

## Where I would still keep a human firmly in the loop

Real-time interaction quality, security boundaries, network behavior under hostile conditions, dependency choices, UX tradeoffs, and whether a feature is worth building are not things I want to outsource to a benchmark score. A capable model can widen the amount of surface area one person can cover; it does not remove responsibility for the surface area.

For me, that is the point of VESPER as a showcase: it is small enough to inspect and run, but broad enough that coherence matters.

**Solo demo:** [Open in the browser]({{ '/demos/vesper/' | relative_url }})
