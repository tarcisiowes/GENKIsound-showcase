
## README — `GenkiSound-showcase`

```md
# GenkiSound

A mobile music product focused on mood-based playback, safe audio modulation, streaming integrations, and music-learning interactions.

> This public repository is a product showcase. The production codebase is private.
> This repo focuses on product scope, architecture, technical decisions, and delivery direction.

---

## Overview

GenkiSound explores a specific product idea: helping users interact with music through mood-based playback controls and learning-oriented experiences without turning audio manipulation into a gimmick.

The product began around a focused playback concept:

- adjust a track toward a more relaxed or more energetic feel
- keep tempo and pitch changes inside safe ranges
- make playback controls understandable and predictable
- support a path toward richer music-learning flows

Over time, the product also expanded into:

- streaming-provider integrations
- lyrics-first learning surfaces
- guest-first review and sync flows
- feedback and account tooling
- focus-session support

---

## What makes it different

- **Mood-based playback** instead of generic equalizer-style controls
- **Safe tempo and pitch modulation** with explicit quality boundaries
- **Music-learning interactions** layered into the playback product
- **Guest-first architecture** instead of hard login gating
- **Streaming-aware design** across Spotify and YouTube paths
- **Native-first audio direction** for long-term DSP flexibility

---

## Core Product Areas

- Mood presets
- Manual tempo and pitch controls
- Playback queue and transport controls
- Streaming screen and provider switching
- Lyrics-first learning and review handoff
- Guest-first account and sync foundation
- Focus timer / session support
- Feedback and error-log support

---

## Screenshots

> Screenshots will be added later.

Suggested structure:

- `docs/screenshots/home.png`
- `docs/screenshots/player.png`
- `docs/screenshots/streamings.png`
- `docs/screenshots/music-learning.png`
- `docs/screenshots/review-hub.png`
- `docs/screenshots/config.png`

---

## Navigation GIF

> A navigation GIF will be added later.

Suggested placement:

- `docs/gifs/genkisound-navigation.gif`

---

## Simple Architecture Diagram

```mermaid
flowchart TD
    A[React Native CLI App] --> B[Navigation + Screens]
    A --> C[Audio Engine Contract]
    C --> D[Mock / Native Audio Adapter]
    A --> E[Playback Domain Logic]
    A --> F[Streaming Layer]
    F --> G[Spotify]
    F --> H[YouTube]
    A --> I[Guest-first Review + Sync]
    I --> J[SQLite Local State]
    I --> K[Supabase]
    A --> L[Notifications / Focus Sessions]
    A --> M[Feedback + Error Logging]
