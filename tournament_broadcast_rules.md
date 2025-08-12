# Twitch Production Flow.md

## Purpose
This guide defines the live streaming structure, camera/audio routing, and production timing for **Strict** (tournament) and **Casual** (community) formats.  
Optimized for OBS/Streamlabs/XSplit setups.

## Quick View: Core Feeds
Every format uses the same **core feed set**, but how they’re mixed differs.  

| Feed Name | Description |
|-----------|-------------|
| **Guardian POV (x2)** | One per Soul Guardian. Shows their board view + microphone audio. |
| **Guardian Internal** | Private feed for confession booth or personal monologue. |
| **NPC Team POV (x2)** | Internal team view + mic audio. No Guardian voices. |
| **Commentator Booth** | Video + audio commentary. Receives only game state visuals. |
| **Game State Cam** | Top-down board view; may be digital or physical camera. |
| **Main Broadcast Mix** | Producer-selected combination of feeds for the public stream. |

## Strict Format Production Flow

### 1. Pre-Match
- **Main Broadcast**: Introduce teams, format, and stakes.  
- Camera cycling between commentators, Guardians’ intro shots, NPC team reaction shots.

### 2. During Play
- **Guardians’ Comms**: Muted from public feed; only visuals are shown unless confession booth is active.
- **Confession Booth Activation**:  
  - Triggered by Guardian request or producer prompt.
  - Guardian feed switches to *Guardian Internal* audio.
  - Clip recorded, stored on delay buffer (e.g., 30–120 sec).
  - Only played later during replay/highlight moments.
- **NPC Teams**:
  - Private team channel.
  - Producer only switches to NPC POV for *visual drama*, never live audio in strict.
- **Commentators**:
  - Receives live *Game State Cam* + turn timer info.
  - Never hear live player comms.
  - Can narrate over replayed confessionals.

### 3. Parlay Phase
- **Strict Rules**: Parlay session is judge-moderated.  
- Producer can fade in NPC POV audio briefly to public feed.  
- All parlay clips stored for recap package.

## Casual Format Production Flow

### 1. Pre-Match
- Intro sequence similar to strict, but producers can *immediately* sample banter from Guardians or NPCs to set the tone.

### 2. During Play
- **Guardians’ Comms**: Permanently live in each Guardian POV stream.  
  - Public main broadcast *may* mix both into a split-screen view for highlight moments.
- **Internal Monologue**:
  - Always hot-mic on personal POV.
  - Producer can cut to Guardian Internal feed *in real time* for viewers.
- **NPC Teams**:
  - Open mics during their turn.
  - Freeform parlay audio often mixed into the main broadcast for entertainment.
- **Commentators**:
  - Still game-state only.
  - May be fed delayed clips of comms to react live for added entertainment.

### 3. Parlay Phase
- Informal and chaotic.
- Producer actively switches between NPC POVs, main board cam, and commentator reactions for maximum drama.

## 4. OBS / Production Setup Map

### Scene Groups
1. **Main Match Scene**:
   - Top-down game state cam
   - Sidebars with Guardian/NPC reaction shots
2. **Guardian POV Scene**:
   - Single Guardian cam full-screen + board overlay
3. **NPC POV Scene**:
   - NPC team full-screen with scoreboard overlay
4. **Commentator Scene**:
   - Booth cam with game state in picture-in-picture
5. **Confession Booth Scene**:
   - Solo Guardian feed with thematic frame + sound isolation
6. **Parlay Scene**:
   - Split screen of both NPC teams or both Guardians (depending on rule format)

## 5. Live Switching Guidelines
- **Strict**:
  - Maintain narrative tension; avoid revealing strategic comms.
  - Cut confession booth segments in for dramatic moments.
- **Casual**:
  - Switch aggressively for banter and live reactions.
  - Prioritize high-energy player/NPC audio over prolonged game-state shots.
