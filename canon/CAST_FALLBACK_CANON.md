# CAST FALLBACK — CANON

_Status: CURRENT CANON_
_Date: 2026-09-14_

## Purpose

A dedicated TV app is the preferred shared-display experience, but the game must also provide a **casting fallback** for compatible televisions and streaming devices.

The casting path is a **basic shared-table presentation**, not a feature-identical replacement for the native TV app.

The goal is accessibility: players should be able to play on a compatible TV even when no native LOTR TV app exists for that platform.

---

## Preferred Display Order

1. **Native TV App** — full shared-table experience.
2. **Compatible Cast Receiver** — lightweight/basic shared-table experience.
3. **Player Device Table View** — complete functional fallback if no TV path is available.

Gameplay rules, state and outcomes remain identical across all three. Only presentation capability changes.

---

## Casting Architecture

The cast receiver is a thin presentation client connected to the same authoritative game server as the native TV app and Player Consoles.

A player's phone/tablet initiates the cast/pairing session. After connection, the receiving television/device becomes a passive shared display.

The casting phone is **not the authoritative game host** and should not be required to continuously render or mirror the board pixel-for-pixel.

Where the platform permits, use a receiver-style application/page that receives authoritative game state directly from the server rather than traditional screen mirroring.

This preserves the core architecture:

**server decides → shared display presents → phones control**

---

## Basic Presentation Scope

The cast experience should prioritize clear gameplay over visual richness.

Required/basic features:

- World View map;
- Hero/company portrait markers;
- Greater Region state;
- internal Position occupancy when relevant;
- region control / contested state;
- corruption / Shadow state;
- current turn and active Hero focus;
- movement visualization;
- battle result presentation;
- retreat visualization;
- Event / Movement-card reveal presentation;
- victory/end-state presentation;
- essential shared audio if practical.

The basic cast renderer may reduce or omit:

- HDR10 output;
- advanced particles;
- dense atmospheric layers;
- high-resolution region animation;
- complex shader effects;
- elaborate semantic camera transitions;
- premium ambient animation;
- very high-resolution asset packs;
- other effects that are expensive or unreliable in a cast/web receiver environment.

It should still feel like the same game, not a debug screen.

---

## Asset Tier

Casting should use a deliberately lighter presentation pack, for example:

- simplified world map textures;
- lower-resolution region art;
- reduced animation frame count;
- fewer composited corruption layers;
- lighter audio package;
- simplified effects;
- SDR-first output.

The server/manifest system may advertise a dedicated capability tier such as:

`cast-basic`

This tier affects presentation only and never rules or available gameplay information.

---

## Casting Compatibility

Casting support should target compatible receiver ecosystems where technically practical, including TVs or streaming devices that expose appropriate casting/receiver functionality.

Compatibility is capability-based rather than brand-exclusive.

A compatible TCL/Android TV may use the native Android TV app when installed, while the casting path remains available as a fallback or quick-start option.

---

## Pairing / Launch

Preferred flow:

1. Player creates/joins a game on phone/tablet.
2. Player chooses **Play on TV**.
3. Available native/pairable/cast displays are presented where platform APIs permit.
4. If a native TV app is available, it is preferred.
5. Otherwise a compatible cast receiver is launched.
6. Shared display connects to the authoritative session.
7. Player continues using the phone/tablet normally.

The goal is minimal television-side interaction.

---

## Failure / Recovery

If casting disconnects, gameplay must continue on player devices.

The cast display may reconnect and reconstruct current presentation state from the authoritative server without restarting the game.

A failed cast session must never corrupt or own game state.

---

## Canon Rule

**Casting is a compatibility fallback, not the premium presentation target.**

**Native TV app = cinematic living table. Cast receiver = clear, lightweight shared board.**
