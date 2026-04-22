# Architecture Summary

GenkiSound is built as a React Native CLI product because audio control and future DSP depth are core to the product direction.

## App Layer

- React Native CLI
- TypeScript
- navigation-driven mobile app structure
- reusable playback and control components

## Audio Layer

- explicit `AudioEngine` abstraction
- mockable development path
- native adapter direction for real playback and modulation
- safe tempo and pitch control domain rules

## Domain Layer

The domain layer focuses on behavior that should remain predictable and testable:

- clamp logic
- preset logic
- mood presentation rules
- playback queue behavior
- review and progression-related logic

## Data and Account Layer

- local persistence for guest-first progress
- Supabase-based auth and sync layer
- secure provider/account state handling

## Integration Layer

- Spotify App Remote + Web API
- YouTube iframe and related service helpers
- local notifications
- secure storage and auth session handling

## Architectural Direction

The product is intentionally biased toward native flexibility:

1. protect audio quality before adding aggressive effects
2. keep playback logic separate from screen code
3. support guests before forcing account friction
4. treat streaming providers as integrated product surfaces
5. preserve room for future DSP and premium expansion
