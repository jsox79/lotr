# TV APP ARCHITECTURE — CANON

_Status: CURRENT CANON_
_Date: 2026-09-14_

## Product Direction

Ship a dedicated TV application where practical.

The TV application is a **lightweight rendering client**, not the authoritative game engine and not a duplicate of the phone/tablet player application.

Its job is to connect, cache, render, animate, play sound and present authoritative game state beautifully on the shared display.

The game server remains authoritative for rules, RNG, decks, combat, movement legality, control, corruption, HP, victory conditions and all other game logic.

---

## Thin-Client Principle

The installed TV package should contain only what is needed to boot and operate reliably:

- rendering/runtime code;
- networking and session connection logic;
- pairing UI;
- local asset cache manager;
- basic loading/offline/error presentation;
- fonts and minimal shell UI assets;
- platform integration required for lifecycle, storage, display and audio.

Large or game-specific content should be delivered from the server/CDN rather than baked permanently into the application package.

Server-delivered content may include:

- world map artwork;
- region artwork;
- internal Position art/state;
- Hero portraits and corruption variants;
- Allies, Enemies and Lesser Location art;
- corruption/Shadow overlays;
- environmental animation layers;
- card art;
- particles/effects;
- sound and music assets;
- region-scene assets;
- presentation data and other content packs.

This allows art/content updates without requiring a full TV app release every time.

---

## Asset Manifest

At startup the TV client receives or fetches a versioned asset manifest describing the content pack required for the current game/client version.

Example concept:

```json
{
  "assetPack": "middle-earth-v0.14.2",
  "map": "map/world-v7",
  "regions": "regions-v11",
  "heroes": "heroes-v8",
  "shadow": "shadow-layers-v4",
  "audio": "audio-v3"
}
```

Assets should use stable IDs plus content hashes/versioning so the client can determine exactly what changed.

The TV downloads only missing or changed assets.

---

## Persistent Local Cache

Assets are cached aggressively on the TV after download.

A typical cache may contain groups such as:

```text
/cache
  /world
  /regions
  /heroes
  /allies
  /enemies
  /locations
  /effects
  /audio
```

If an asset's hash/version has not changed, it should not be downloaded again.

Normal startup should therefore be:

**launch → connect → compare manifest → fetch deltas → join table**

rather than redownloading the entire game presentation every session.

Cache invalidation must be explicit and version/hash driven.

---

## Intelligent Prefetch

The TV client should prefetch likely-needed assets before they become visible.

Examples:

- when a Hero begins moving toward Rohan, prefetch uncached Rohan Region View assets;
- when a battle becomes imminent, prefetch combat presentation assets;
- when a corruption threshold approaches, prefetch the next visual corruption state if needed.

Prefetching should prioritize seamless presentation without delaying authoritative game resolution.

---

## Authoritative Event Stream

The TV never determines game outcomes.

The server sends authoritative state and events such as:

- `battle.started`
- `battle.result`
- `damage.assigned`
- `force.retreat`
- `position.control_changed`
- `region.control_changed`
- `region.corruption_changed`
- `movement.started`
- `movement.resolved`
- `event.revealed`
- `victory.triggered`

The TV interprets those events visually and audibly.

Example:

```json
{
  "type": "region.corruption_changed",
  "region": "rohan",
  "from": 2,
  "to": 3
}
```

The TV may animate/interpolate from one visual state to another, but the underlying state comes only from the server.

### Canon Rule

**The TV makes outcomes visible; it does not decide outcomes.**

---

## Pairing / Table Join

TV onboarding should require minimal or no remote interaction after launch.

Preferred flow:

1. TV app launches.
2. TV displays a short table code and/or QR code.
3. A player's phone creates or joins the game and pairs the TV.
4. The TV becomes the shared display for that game session.
5. Players continue controlling the game from their phones/tablets.

The TV should not require routine account navigation, deck management or gameplay input with a television remote.

After pairing, the TV should behave as an appliance-like shared game table.

---

## Platform Strategy

Preferred implementation direction:

1. Android TV / Google TV first.
2. Fire TV shortly afterward where practical because of platform similarity.
3. Samsung Tizen.
4. LG webOS.

The goal is **one shared table renderer with thin platform shells**, not four independently implemented visual clients.

Conceptually:

```text
             SHARED TABLE RENDERER
                    |
        +-----------+-----------+
        |           |           |
   Android TV     Tizen       webOS
      shell        shell        shell
```

Platform shells handle environment-specific concerns such as:

- application lifecycle;
- persistent storage/cache;
- network APIs;
- display modes;
- HDR capability detection;
- audio/device integration;
- remote/back-button behavior;
- store/package requirements.

Game-state visualization and core rendering behavior should remain shared wherever technically practical.

---

## Resolution / Display Targets

Recommended consumer display target:

- **Minimum functional:** 43-inch, 1080p.
- **Minimum recommended:** 55-inch.
- **Primary design target / sweet spot:** 65-inch, 4K.
- **Large-room premium:** 75–85-inch.

The world-view UI must remain readable at ordinary couch viewing distances.

The renderer should scale detail and marker density according to effective resolution and display capability.

---

## SDR and HDR10

The game must remain fully functional and readable in SDR.

HDR is an enhancement layer, not a gameplay requirement.

Preferred presentation tiers:

- 1080p SDR;
- 4K SDR;
- 4K HDR10.

HDR10 is the preferred open HDR target.

Dolby Vision is not a requirement.

HDR may enhance:

- luminance contrast between Light and Shadow;
- Mordor fire/lava;
- Galadriel/Lothlórien light effects;
- Phial/holy/light effects;
- deep-Shadow environments;
- corruption transitions;
- atmospheric weather and magic.

Gameplay state and legibility must remain equivalent in SDR and HDR.

---

## Capability Reporting

The TV client may report presentation capabilities such as:

- effective resolution;
- HDR10 support;
- approximate GPU/performance tier;
- memory/cache tier;
- platform/runtime version.

The asset server may then select an appropriate content tier, for example:

- lightweight 1080p SDR pack;
- 4K SDR pack;
- 4K HDR10 pack.

This must never alter game rules or hidden game information; it only changes presentation quality.

---

## Separation from Player Console

The TV app and phone/tablet Player Console have different responsibilities.

### TV App

- shared/public state;
- living map;
- camera focus;
- Hero/company markers;
- Region View;
- battles and retreats;
- corruption/world transformation;
- Event presentation;
- shared audio/atmosphere.

### Player Console

- private hand;
- private choices;
- detailed character/stack interaction;
- down-right card stack language;
- stats/counters/corruption detail;
- action selection;
- private information and confirmations.

The TV app is **not** a port of the phone app.

---

## Reconnect / Recovery

The TV is disposable presentation state.

If the TV app is restarted, crashes, loses network connectivity or another display replaces it, it reconnects to the authoritative server and reconstructs presentation from current game state.

No critical game state should exist only on the television.

---

## Design North Stars

**The TV is a lightweight window into the authoritative table, not the table's brain.**

**Install the renderer once; deliver the world from the server.**

**The television should feel like a dedicated Middle-earth game console after pairing.**
