# DIGITAL CARD & STACK LANGUAGE — CANON

_Status: CURRENT CANON_
_Date: 2026-09-14_

## Core Principle

**The card is display. The companion interface is state.**

Cards remain visually clean and art-forward. Detailed game state is not permanently printed or overlaid onto the card face simply because the game is digital.

The card face presents the character or object. The Player Console presents detailed rules and live state such as counters, Corruption, modifiers, attachments, abilities, and other mechanical information.

---

## Hero Card Face

The established Hero-card visual language is preserved digitally:

- full-bleed portrait artwork;
- no conventional rules textbox;
- no heavy frame or dashboard furniture;
- character name anchored at the lower-right;
- Strength and Health anchored at the lower-left;
- combat/stat emblem between the lower-left values where appropriate;
- artwork remains the dominant visual element.

The normal card face should not become cluttered with corruption counters, temporary modifiers, ability text, faction banners, or other companion-interface data.

---

## Stack Direction

Player stacks cascade **down and to the right**.

The **Active / Main Hero is always the leading anchor card**.

At rest:

- the Active Hero occupies the bottom-most foundational stack position;
- visually, the Active Hero is the upper-left leading card and is always shown by default;
- every attached / accompanying stack card occupies a progressively down-right position behind it;
- enough of each subsequent card remains exposed to communicate that it exists and to permit selection;
- no normal stack member naturally rests in front of the Active Hero.

A stack therefore communicates both identity and party composition at a glance: the Active Hero identifies the force, while the down-right cascade shows that additional cards belong to that Hero's stack.

---

## Card Interaction Cycle

Every selectable card uses the same fundamental interaction metaphor:

**STACK → FOREFRONT DISPLAY → STATS / STATE → DISMISS / RETURN**

### 1. Stack State

The card rests in its canonical stack position.

For the Active Hero this is the leading anchor position. Supporting cards remain in their assigned down-right stack positions.

### 2. First Tap — Forefront Display

Tapping any exposed card pulls that card out of the stack and gives it the visual forefront.

- The selected card becomes the dominant card on screen.
- The full card artwork is presented cleanly.
- No detailed statistics panel is required yet.
- Other cards remain logically in their stack positions even while the selected card is temporarily foregrounded.

This state is equivalent to physically picking a card up from the table to look at it.

### 3. Second Tap — Stats / State

Tapping the foreground card again transitions to its detailed game view.

- The artwork/card shrinks or repositions rather than disappearing.
- The Player Console exposes the card's complete relevant live state.
- For a Hero this can include current Health, Strength and modifiers, Corruption, counters, abilities, Artifacts, Gear, Rings, Bannermen, Allies, Titles, Boons, temporary effects, faction effects, movement state, and other applicable mechanics.

The exact information depends on card type.

### 4. Third Tap — Dismiss / Return

Tapping again dismisses the detailed view.

The card returns to its exact canonical resting position:

- a single Active Hero returns to the leading Hero position;
- a card belonging to a stack returns to its exact stack index / slot;
- the original down-right stack ordering is restored.

Selection never permanently changes stack order merely because a card was inspected.

---

## Stack Ordering Rule

The Active Hero is always the visual and mechanical anchor of a player stack.

Supporting Heroes / Bannermen, Allies, Artifacts, Titles, Boons, and other stack members may occupy defined positions behind the Active Hero according to stack-order rules, but none supersede the Active Hero's leading position at rest.

A selected card may temporarily appear above the Active Hero and all other stack cards. This is a presentation state only and does not alter stack ownership, hierarchy, or order.

---

## Digital State Requirement

The software must preserve enough information to restore a selected card precisely after dismissal, including at minimum:

- card identity;
- owning player;
- stack identity;
- stack index / logical position;
- Active Hero relationship;
- region / location;
- attachment relationship where applicable.

Rendering coordinates are derived from this logical state. The rules engine must not use temporary foreground/display coordinates as game state.

---

## Shared Table vs Player Console

The same stack language may be used on the shared Table View in a more compact form.

The Table View should emphasize the Active Hero / leading stack identity and enough of the cascade to communicate force size and composition without turning the television into a detailed character sheet.

The private Player Console is where a player performs the full tap cycle and inspects detailed private or mechanical state.

---

## Design North Star

**Cards display the world. The companion interface displays the rules and state.**

The digital implementation should preserve the feeling of handling a beautiful physical card rather than replacing the card with a conventional software panel.
