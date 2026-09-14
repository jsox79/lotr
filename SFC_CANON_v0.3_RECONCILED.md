# Shadow & Fellowship — Canon v0.3 Reconciled

_Status: CURRENT WORKING CANON_
_Date: 2026-09-14_

This document supersedes `SFC_CANON_v0.1_reconciled.zip` as the top-level reconciliation authority.

The v0.1 ZIP remains historical source material. Rules and content from it remain inherited unless explicitly changed by this document or by a newer file under `/canon/`.

## Canon Priority

1. Newest explicit canon file under `/canon/`.
2. This reconciliation document.
3. Reconciled v0.2 design decisions recorded in project history.
4. `SFC_CANON_v0.1_reconciled.zip` for inherited material not otherwise superseded.

Omission is NOT deletion. Any named character, rule object, region, faction, card, location, artifact, enemy, Ally, title, boon, or mechanic mentioned in prior canon remains preserved until explicitly removed.

---

# 1. Game Identity

Shadow & Fellowship is a fully digital tabletop strategy game centered on:

- stacking Heroes, Bannermen, Allies, Artifacts, Titles, Boons, and other effects into powerful regional forces;
- controlling Greater Regions;
- moving those stacks through Middle-earth;
- resolving uncertain regional travel;
- choosing when to initiate conflict;
- managing or intentionally embracing Corruption;
- pursuing standard, Ring-based, Dominion, Shadow, or character-specific victory conditions.

Core design statement:

**Stacking builds power. Regional control wins games. Movement creates risk. Corruption creates temptation. Combat changes ownership.**

---

# 2. Digital Tabletop Architecture

The prior physical-card + companion-PWA architecture is retired.

The current architecture is:

- **Shared Master Map / Table View** on a TV or shared display.
- **Private Player Console** on each player's phone or tablet.
- **Authoritative Game Server** that owns rules, RNG, decks, hidden information, turn state, combat, movement, corruption, and victory checks.

A player can open or cast the shared Table View to a television while continuing to use the same phone/tablet as their private controller.

The television is not the host. It is a public view of the same server-owned game session.

Private information is never transmitted to other players or the Table View merely to be hidden visually.

---

# 3. Living Master Map

The Master Map is a live game scene, not a static board image.

It should visually represent:

- the 10 Greater Regions;
- region control;
- regional Corruption;
- Active Heroes;
- Bannermen;
- Ally forces;
- Enemies;
- Lesser Locations;
- Artifacts / major state where publicly relevant;
- battles and skirmishes;
- Events;
- movement between regions;
- atmospheric changes caused by Corruption and world state.

The TV normally shows a world view and may automatically focus on a region for important movement, encounters, battles, and Events.

---

# 4. Character Preservation

All named characters previously mentioned are preserved unless deliberately removed.

Current known Hero-character roster includes:

- Frodo
- Sam
- Merry
- Pippin
- Gandalf
- Elrond
- Galadriel
- Legolas
- Aragorn
- Boromir
- Faramir
- Denethor
- Théoden
- Éomer
- Éowyn
- Gimli
- Dáin
- Thorin Stonehelm
- Treebeard
- Saruman
- Gríma Wormtongue

Gollum is preserved separately as a Special Character / disruption card, not a Hero.

Where an older detailed character entry exists and a later reconciliation accidentally omitted that character, the detailed entry remains recoverable canon and must be reconciled rather than treated as deleted.

---

# 5. Corruption as Choice

Corruption is temptation, not only punishment.

When a corruptible Hero reaches their Corruption Limit, the controller chooses between:

## Reject the Shadow

- The Hero is destroyed.
- The player continues through remaining Heroes / strategy.

## Embrace the Shadow

- Flip to the Hero's corrupted form.
- The Hero remains player-controlled.
- The corrupted form receives substantially greater power.
- The corrupted form also incurs a major loss, restriction, liability, changed allegiance, or changed objective.
- A character-specific corrupted victory condition may become available.

The choice should be genuinely tempting. Corruption must not be obviously always bad or obviously always superior.

Galadriel remains the model case: tremendous power as Lady of Shadow in exchange for becoming a territorial corruption engine with an altered route to victory.

Frodo remains a special case and cannot simply choose a corrupted reverse form.

---

# 6. Stacking and Regional Control

The game is fundamentally about building and moving stacks.

A player's regional force may include:

- one Active Hero;
- Bannermen / Supporting Heroes;
- Allies;
- Artifacts / Gear / Rings;
- Titles / Boons;
- temporary or persistent effects.

Regional control is distinct from mere presence.

Multiple players may be present in the same Greater Region without immediately fighting.

Entering, occupying, or passing through another player's controlled region does **not** automatically initiate battle.

Combat between player forces is deliberate unless a specific card, Enemy, Event, region rule, or scenario explicitly forces it.

This permits passage, diplomacy, temporary coexistence, threats, bluffing, and strategic positioning.

## Digital Stack Presentation

The canonical digital card and stack interaction language is defined in `canon/DIGITAL_CARD_STACK_LANGUAGE_CANON.md`.

Key locked rules:

- the card itself is display; the Player Console carries detailed live state;
- the Active / Main Hero is always the leading anchor card and is shown by default;
- stacks cascade down and to the right behind the Active Hero;
- no ordinary stack member rests in front of the Active Hero;
- first tap pulls any exposed card to the visual forefront as clean full-card art;
- second tap transitions to the card's detailed stats / state view;
- third tap dismisses it and restores its exact stack position;
- temporarily foregrounding a card never changes its logical stack order.

---

# 7. Movement

Movement follows the Greater Region adjacency graph.

Crossing a regional boundary triggers that destination region's Movement Deck.

A Movement card is drawn:

- when entering a Greater Region from another Greater Region;
- when passing through a Greater Region during multi-region movement.

A Movement card is NOT drawn merely for beginning a turn in a region or remaining stationary.

Leaving and later re-entering a region triggers a new Movement draw.

Movement does not inherently cause player-versus-player combat.

---

# 8. Regional Movement Decks

Each Greater Region has its own persistent shuffled Movement Deck.

Movement cards represent what happens while traveling through that specific region.

Initial movement-card families:

- **Discovery** — treasure, Artifact, useful find, healing, information, Ally, or other benefit.
- **Skirmish** — travel encounter with an Enemy or Creature.
- **Delay** — movement stops or is hindered.
- **Speed Boon** — additional or improved movement.
- **Retreat** — return to the previous region and regroup.
- **Hazard** — Damage, Corruption, discard, or other travel cost.
- **Encounter** — character, location, or story interaction.
- **Quiet Passage** — no major harm, possibly a minor benefit.
- **Betrayal** — separation, mistrust, or loss involving a member of the traveling stack.

The decks must be region-specific. The Shire should not feel like Mordor with different artwork.

Regional control and Corruption may alter the outcome of Movement cards without requiring physically separate card versions.

---

# 9. Travel Skirmish vs Battle

A **Skirmish** is an encounter generated by travel or another world effect.

A **Battle** is conflict involving established forces / stacks.

A **Player Attack / Challenge** is a deliberate decision to initiate conflict against another player's force or claim.

Traveling through a region containing another player's units does not by itself create a Battle.

---

# 10. Secret Stair

**Secret Stair** is a rare Mordor-region Movement card / Travel Boon.

When discovered, it may be retained rather than resolved immediately.

Once per game, discard Secret Stair to make one free movement from a region adjacent to Mordor into Mordor.

That movement:

- costs no normal movement;
- bypasses the normal Mordor entry cost or restriction;
- does not draw a Mordor Movement card for that specific entry.

Secret Stair does not bypass Enemies, player forces, region control, or consequences that already exist inside Mordor.

Secret Stair is a Travel Boon, not an Artifact attachment.

---

# 11. Crumbs on His Jacketses

**Crumbs on His Jacketses** is a Mordor-region Betrayal Movement card.

Its purpose is to create separation and mistrust inside a traveling stack.

Current mechanical direction:

- choose a Bannerman / Supporting Hero or Ally traveling with the Active Hero;
- that character is separated from the traveling stack and returns to / remains in the previous region;
- the Active Hero's movement ends and the party must regroup.

Exact wording and any Corruption interaction remain subject to balance testing.

This card does not require Gollum to be a controllable companion.

---

# 12. Gollum

Gollum is intentionally **not strategic inventory**.

He is random disruption: a "shit the bed" card.

**Gollum — Special / Unique Disruption**

Copies: 3 in the Universal Deck unless later tuning changes the count.

When Gollum is drawn, reveal and resolve him immediately.

If the One Ring is in any player's hand or attached to any Hero:

- Gollum takes it;
- remove the One Ring from that player / Hero;
- shuffle the One Ring back into the Universal Deck;
- this cannot be prevented, redirected, saved, retained, targeted, or strategically deployed.

If nobody currently possesses the One Ring:

- Gollum produces no mechanical effect;
- present a brief humorous Gollum interruption / complaint;
- discard him.

Gollum is then discarded.

He is not an Ally, Bannerman, companion asset, retained Scheme, or player-controlled tool.

Design intent: the Ring is powerful but never completely safe. Gollum should appear unpredictably and potentially ruin a Ring strategy at exactly the worst moment.

---

# 13. Universal Deck

The Universal Deck remains a central shared deck for applicable Heroes, Events, Enemies, Lesser Locations, Artifacts, the One Ring, Gollum, and other global content as defined by detailed canon.

Regional Movement Decks are **separate from the Universal Deck**.

They are tied to Greater Regions and are only drawn because of movement into / through those regions.

This distinction is canonical.

---

# 14. Rules Pending Exact Reconciliation

The following are preserved but still require exact normalization before the digital rules engine is considered executable:

- exact 34-card Enemy copy distribution;
- exact Ally roster mechanics and copies;
- exact Regional Movement Deck contents and counts for all 10 regions;
- exact numerical region Corruption maxima / resistance mechanics;
- final rules for deliberate player attacks and timing;
- exact control thresholds / claiming rules where older sources conflict;
- final character-specific corrupted victory conditions beyond already-defined cases;
- final Universal Deck count after all preserved characters and card copies are reconciled.

These gaps are not permission to invent silently. They should be resolved explicitly and then recorded in canon.

---

# 15. Current Software Direction

The application/software layer is being redesigned from scratch around the fully digital tabletop model.

Recommended separation:

- game core / rules engine;
- authoritative multiplayer server;
- shared living Table View;
- private phone/tablet Player Console;
- data-driven content definitions;
- persistent save / reconnect state;
- machine-readable stable content IDs.

The game core must not depend on rendering technology.

---

END OF SFC_CANON_v0.3_RECONCILED
