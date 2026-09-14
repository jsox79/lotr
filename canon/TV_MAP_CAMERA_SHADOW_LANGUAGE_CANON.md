# TV MAP, CAMERA & SHADOW VISUAL LANGUAGE — CANON

_Status: CURRENT CANON_
_Date: 2026-09-14_

## Shared TV Board

The shared TV uses a geographically recognizable but gameplay-optimized Middle-earth map.

- Preserve recognizable relative geography, terrain, mountain chains, forests, rivers, landmarks and regional relationships.
- Distort scale and spacing where necessary to make all Greater Regions useful contiguous gameplay spaces.
- Greater Regions are fully articulated illustrated territories, not abstract boxes or simple colored polygons.
- At world scale, player forces are represented primarily by Hero portrait/head markers rather than full cards.
- A Hero marker represents the Hero and the company/stack traveling with that Hero.
- Public company size/state may be communicated compactly around the marker.
- Selecting a Hero on the TV may expand that force into a clearly visible party tableau beneath/around the lead Hero without changing the underlying stack.

## Semantic Camera / Zoom

The TV camera is an active part of game communication.

Canonical camera levels:

1. **World View** — entire gameboard, regional state, Hero markers, major threats and control.
2. **Turn Focus** — camera smoothly focuses on the active Hero's region and relevant adjacent movement space.
3. **Region View** — camera pushes into a fully articulated Greater Region when an encounter, battle, Movement card, Event, claim, major corruption change, or other important action occurs.

Zooming reveals progressively richer public information rather than switching to an unrelated board. The world and region views are representations of the same authoritative game state.

Region View may expose named locations, roads, terrain, Lesser Locations, separated forces, Enemies, encounters and environmental state that are summarized at world scale.

## Progressive Shadow — Regions

Corruption / Shadow should be visible as a progressive environmental transformation, not merely a number or colored outline.

The renderer should support continuous or stepped visual intensity derived from authoritative region Corruption state.

Suggested visual progression:

- **Clean / Low Shadow:** normal regional artwork, healthy vegetation, normal sky/light, clean water and architecture.
- **Touched:** subtle desaturation, longer/darker shadows, faint haze, isolated dead vegetation, slightly colder or sicklier light.
- **Spreading:** visible dark atmospheric overlay, damaged vegetation, smoke/mist, darker water/soil, architecture beginning to decay, more ominous ambient movement.
- **Deep Shadow:** substantial environmental degradation, oppressive lighting, ash/fog, corrupted vegetation, stronger Shadow visual motifs and increased ambient effects.
- **Fully Corrupted:** region is unmistakably transformed by Shadow while retaining enough original geography and landmarks to remain identifiable and playable.

This should be implemented as layered state where practical rather than requiring a completely separate painted map for every corruption value. Potential layers include color grading, shadow/vignette masks, fog/smoke/ash particles, vegetation/decal swaps, water/sky changes, animated ambient effects, landmark variants and corruption-specific lighting.

Region identity must remain visible beneath corruption. Corruption transforms a place; it should not make every region visually identical to Mordor.

## Progressive Shadow — Characters

Corruptible Heroes should also visually transform as their Corruption rises.

Character corruption should be communicated through progressive portrait/card/marker variants or composited overlays while preserving character recognizability.

Possible layers include:

- reduced warmth / increasing pallor;
- deeper facial and eye shadows;
- exhaustion, stress and increasingly severe expression;
- darkened or degraded clothing/armor;
- subtle Shadow haze or edge treatment;
- progressively unnatural eye treatment;
- spectral / wraithlike cues for appropriate characters;
- final corrupted-form artwork when the Hero Embraces the Shadow.

The transformation should be character-appropriate rather than applying one identical filter to every Hero.

### Men

For corruptible Men, the visual trajectory may increasingly evoke a **Ringwraith-like / wraithbound appearance** as Shadow deepens: pallor, hollow or shadowed features, increasingly spectral eyes, darkening attire/armor, loss of healthy warmth, and an emerging sense that the person is being consumed by Shadow.

This is a visual progression, not a rule that every corrupted Man literally becomes a Nazgûl. Exact final corrupted forms remain character-specific.

### Other Peoples / Characters

Other characters should corrupt according to their own identity and temptation. Galadriel, Gandalf, Saruman and other non-Men should not simply receive the same Ringwraith treatment. Their visual corruption should express the nature of their power, loss and corrupted form.

## Marker Synchronization

Hero portrait markers on the TV should reflect meaningful corruption state so players can read danger at world scale. The marker may use the same progressively corrupted portrait source as the Hero card, supplemented by restrained state effects around the marker.

When the camera enters Region View, the richer corruption treatment becomes more visible. On the private Player Console, the full Hero card and stats/state view can show the most detailed version.

## Design North Star

**Shadow should be seen consuming the world and its people before the numbers need to be read.**

Corruption remains authoritative game state. Visual overlays communicate that state; they do not determine it.
