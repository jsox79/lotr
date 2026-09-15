# COMPANION TRAVEL MAP — CANON

_Status: CURRENT CANON_
_Date: 2026-09-14_

## Approved Visual Reference

The canonical approved Companion Travel Map artwork is stored at:

`art/reference/companion-travel-map/companion-travel-map-approved-v2.png`

Asset blob SHA: `63882f9dff623ffc784a55cb6084f3de790ae99e`

This exact asset is the visual reference for the Companion Travel Map. It must not be silently replaced by a regenerated concept. Any future approved revision receives a new versioned filename and requires an explicit canon decision.

## Purpose

The clean framed schematic map is the canonical **Companion Travel Map** used on phones/tablets for choosing and planning regional movement.

It is intentionally different from the TV Living Map.

- **Companion Travel Map:** strategic, schematic, interactive, route-focused.
- **TV Living Map:** cinematic, atmospheric, animated, presentation-focused.

The Companion Travel Map answers: **Where do you want to go?**
The authoritative server answers: **Is that movement legal and what happens along the way?**
The TV Living Map answers: **What does the journey look and feel like?**

---

## Framed Geographic Layout

The Travel Map uses the established framed geographic/topology layout rather than a contiguous illustrated atlas.

The layout should preserve the approximate north/south/east/west relationships of the ten Greater Regions while prioritizing clear gameplay topology.

The ten Greater Regions remain:

- Shire
- Rivendell
- Lothlórien
- Mirkwood
- Rohan
- Gondor
- Isengard
- Mordor
- Erebor
- Fangorn

Two non-region frames may be reserved for map legend, title, travel information, round/state information or other useful navigation UI.

---

## Gold Travel Nodes

Legal regional connections are represented by **gold travel dots/nodes** at the relevant connection points between region frames.

A gold node has a strict gameplay meaning:

**Gold node = regional traversal is permitted through this connection.**

No gold node = no ordinary regional traversal through that boundary/connection.

Gold nodes are not decorative map ornaments and must not be placed where they do not represent a legal route.

The authoritative travel graph is data-driven. The visual map reflects that graph rather than determining it.

Cards and abilities may create exceptional movement that ignores or modifies the normal graph, such as **Secret Stair**.

---

## Travel Interaction

During a player's Journey/Travel action:

1. Player opens or enters Travel mode on the companion device.
2. The player's current Greater Region is clearly identified.
3. Legal outgoing travel nodes/destinations illuminate or otherwise become interactive.
4. Illegal destinations remain visually unavailable.
5. Player selects a legal node/destination.
6. Companion may show relevant public movement information, cost, known modifiers and route consequences.
7. Player confirms the movement intention.
8. Server validates the movement.
9. On acceptance, authoritative movement resolution begins and the TV presents the journey.

The companion is an intention/selection surface; it does not independently decide movement legality.

---

## Multi-Region Route Planning

Where movement allowance and rules permit, the companion may support plotting a route across multiple Greater Regions.

Example:

**Shire → Rivendell → Lothlórien → Rohan**

The route planner may show:

- number of regional crossings;
- expected movement cost;
- number of Regional Movement resolutions that will be required;
- known public modifiers/hazards;
- special route effects where relevant.

Planning a route does **not** guarantee arrival at its final destination.

Each regional boundary is resolved independently according to canonical Movement rules. A Movement card, encounter, forced stop, retreat, hazard or other effect may interrupt the planned route.

---

## Movement Deck Integration

Crossing into/through a Greater Region triggers that region's Regional Movement Deck as defined in `MOVEMENT_CANON.md`.

The Travel Map may communicate that a crossing will cause a Movement-card resolution without revealing hidden card contents.

Internal movement between Positions inside the same Greater Region is not regional travel and does not draw a Regional Movement card.

---

## Mobility Identity

The Travel Map should make regional mobility understandable at a glance.

Some Greater Regions may function as crossroads with many legal routes; others may be constrained gateways with only a few or even one ordinary path.

This uneven connectivity is intentional strategic design rather than a defect to normalize away.

Regional control can therefore influence not only territory but access, chokepoints, route choice and strategic mobility.

---

## Relationship to TV Living Map

Travel-planning clutter should remain primarily on the companion device.

The TV does not need to display a permanent network of route lines or destination-selection UI.

Once movement is confirmed, the TV may:

- focus the active Hero/company;
- animate departure;
- show travel/environmental presentation;
- present Movement-card/encounter resolution as appropriate;
- move camera toward the destination;
- show arrival at the correct Region/Position;
- visually respond to interruption, retreat or forced stop.

The TV Living Map may also contain subtle gold connection markers where useful, but its primary purpose remains cinematic shared-state presentation rather than route planning.

---

## Design North Stars

**Phone: Where do you want to go?**

**Server: What happens along the way?**

**TV: Watch the journey happen.**

**Gold travel nodes are rules, not decoration.**

**Some regions are crossroads. Some are gateways. Some are traps.**
