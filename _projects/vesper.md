---
layout: page
title: VESPER · Far Frontier
date: 2026-09-05
project_type: Astra capability demo
description: >
  A self-contained 3D space sandbox with offline solo play, multiplayer server support, modular ships, combat, economy, Docker packaging, and tests.
---

<div class="project-hero">
  <span class="eyebrow">Astra capability demo · 3D web prototype</span>
  <h2>VESPER · Far Frontier</h2>
  <p>A small but complete space sandbox: four worlds, procedural ships, pirates, a modular hangar, economy, and multiplayer for a group of friends.</p>
</div>

<div class="project-actions">
  <a href="{{ '/demos/vesper/' | relative_url }}">Play solo demo ↗</a>
  <a href="{{ '/assets/downloads/VESPER.zip' | relative_url }}">Download full package</a>
</div>

I use **VESPER** in this portfolio as a practical demonstration of what an Astra-assisted end-to-end workflow can look like: not just generating a snippet, but carrying a concept through client code, server logic, packaging, documentation, and repeatable tests.

<div class="callout callout--accent">
<strong>Important framing.</strong> The interesting part is not “AI made a game.” The interesting part is that the result is inspectable and runnable: a static solo client, a small authoritative multiplayer server, Docker packaging, and a test suite. Engineering judgment still lives in the constraints, verification, and decisions around the generated work.
</div>

## What is in the prototype

- Browser-based 3D flight with inertia, boost, braking, collisions, landing, and quantum travel.
- Four planets: Aurora, Ember, Nyx, and Dune.
- Modular ship construction, weapons, shields, armor, fuel, ammunition, damage, repairs, and economy.
- Pirates and optional player-vs-player combat.
- Offline solo mode that runs from static files without npm, a server, or an account.
- Multiplayer for up to eight connected pilots in a room, with a Node.js WebSocket server and persistent room data.
- Docker/Compose packaging for a simple LAN deployment.
- Three.js 0.169.0 and ws 8.18.0 are vendored with their licenses.

## Verification

The repository includes **18 game-rule tests plus one real HTTP/WebSocket integration test** with eight clients. The tests cover movement, fuel, landing, economy, weapons, damage, hostile inputs, room passwords, capacity, persistence, and recovery after restart.

## Why it belongs here

VESPER is useful as a portfolio piece because it crosses multiple layers at once: visual frontend, real-time simulation, networking, persistence, deployment, documentation, and automated verification. It is small enough to inspect, but broad enough to expose whether an AI-assisted workflow can stay coherent across a whole product slice.

The solo demo above is copied into this site as static files, so GitHub Pages can serve it directly. Multiplayer still requires the server included in the downloadable package.
