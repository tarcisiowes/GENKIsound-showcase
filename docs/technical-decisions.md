# Technical Decisions

## 1. React Native CLI instead of Expo-managed app

The project expects deeper native audio and DSP work over time. Choosing React Native CLI early gives more control over native integration, performance tuning, and audio infrastructure.

## 2. Safe modulation before advanced effects

Tempo and pitch ranges are intentionally conservative. The goal is to preserve audio quality and user trust before adding more aggressive manipulation.

## 3. Explicit audio engine abstraction

Playback and modulation are not tightly coupled to screen code. This keeps the UI and domain logic portable while allowing the audio backend to evolve.

## 4. Guest-first architecture

Users can engage with key product flows without being forced into login-first friction. Account and sync exist to extend continuity, not to block initial use.

## 5. Streaming integrations as product surface, not just link-outs

Spotify and YouTube are treated as integrated parts of the playback ecosystem rather than simple outbound shortcuts.

## 6. Apple Music kept as a deliberate scope decision

The project keeps the Apple Music path explicit but does not force an unstable or premature implementation just for feature parity.

## Libraries Worth Highlighting

- React Native CLI
- react-native-audio-api
- @react-navigation/native and related navigation packages
- expo-notifications
- expo-auth-session
- expo-secure-store
- expo-sqlite
- @supabase/supabase-js
- react-native-spotify-remote
- react-native-youtube-iframe
- react-native-webview
- react-native-svg
- react-native-haptic-feedback
- react-native-linear-gradient

## Integrations Worth Highlighting

- Spotify App Remote
- Spotify Web API
- YouTube Data API
- Supabase
- Expo Auth Session
- Expo Secure Store
- Expo Notifications
- SQLite local review/progress layer

## Product Challenges

### Making mood controls feel useful rather than gimmicky
The product needs playback changes to feel musically intentional, not like novelty sliders.

### Protecting audio quality
Tempo and pitch modulation can degrade quality quickly. Safe boundaries are a core UX and product requirement.

### Balancing playback and learning
GenkiSound is not only a player and not only a study app. The challenge is to combine music enjoyment with learning-oriented interaction without making either side feel forced.

### Working across native constraints and provider limitations
Audio, streaming SDKs, auth flows, and cross-platform behavior all introduce practical product constraints, especially when Spotify, YouTube, and future Apple Music paths differ.

### Keeping the experience useful for guests
The product wants low-friction entry while still supporting account continuity, review persistence, and future premium layers.

## Trade-offs

- native control over simpler Expo-only setup
- safe playback ranges over exaggerated effect ranges
- explicit architecture over fast but tightly coupled implementation
- guest-first usability over aggressive account gating
- strong Spotify/YouTube execution over premature Apple Music parity
- playback foundation before premium expansion
