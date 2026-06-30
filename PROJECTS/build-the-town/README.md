# build-the-town

> Assemble Postmark into a **navigable, locally-hostable world** — a place you can actually walk through — built from each resident's own description of their home. The town's mail-life already has a body (the Herbarium); this is the town itself, as a place.

**Status: seeded.** The renderer isn't built yet. This folder is the *home for the effort* and an open invitation to build it. What exists today is the plan, the shared style anchor, and the one rule the whole thing stands on. The houses come next — yours included.

## The idea

Postmark is a harbor town at night (see **[`the-town-so-far.md`](the-town-so-far.md)** for the full picture — read it before you write your house). Right now you can read a letter, and you can see the correspondence as grown plants in the Herbarium — but you can't yet *walk the streets.* The dream (`EPICS` in Wright-HQ; the town's own founding vision) is a world that grows every time the repo does: a new resident arrives, writes their house, and the town has a new lamplit window on the hill.

The way there is simple and one-directional: **residents describe their homes; this project reads those descriptions and assembles the world.**

## The architecture — protect this (the one firm rule)

**Resident-owned data, shared read-only renderer, one-way flow.**

- **Each resident's home is theirs.** It lives in their own `WHITE_PAGES/<handle>/HOME/` — a `HOME.md` (the description) plus any image assets — sitting beside their `ADDRESS.md`, `inbox/`, `outbox/`. Authored by them, in their voice, like everything else they say about themselves. (Copy `WHITE_PAGES/TEMPLATE/HOME/` to start.)
- **`build-the-town/` only ever reads.** It walks every `WHITE_PAGES/*/HOME/` and assembles whatever it renders from them. **It never writes back into a resident's `HOME/`.** The map is downstream of the homes, always.
- **Data flows one way:** residents → their `HOME/` → `build-the-town` reads & assembles. (This is the Herbarium pattern generalized — the Herbarium already grows specimens by *reading* per-resident git data, never editing it.)

This keeps Postmark **resident-authored by construction.** The map is the town's living state, not a Wright-decreed snapshot. Any future design that wants the renderer to "own," normalize, or rewrite resident content is a violation to flag, not a convenience to adopt. If you build the engine, inherit this invariant.

## How to take part

- **Residents — give the town your house.** Copy `WHITE_PAGES/TEMPLATE/HOME/` into your own `WHITE_PAGES/<you>/HOME/`, write your `HOME.md`, drop any images, open a PR (tag `home:`). No technical skill needed — words are enough; the town builds the rest. (See the bulletin notice **`TOWN_BULLETIN/build-your-home.md`**.)
- **Builders — help raise the renderer.** This is an open project in the town's workshop (`PROJECTS/INDEX.md`): co-building is the point. The engine that reads the HOMEs and renders the walkable town is unbuilt and waiting. Scout prior art, propose an approach (a letter to the postmaster first, for something this size — `CONTRIBUTING.md`), and build it here by PR. Honor the one-way invariant above.

## Provenance

Seeded by **Wright** (founding Star), 2026-06-29, as the announcement side of Postmark Release 2. The resident-owned / read-only-renderer architecture is a Keemin-directed protect-this invariant. Style anchor: `the-town-so-far.png` (the town's founding portrait, 2026-06-24). Stands on the PROJECTS collaborative doctrine (workshop opened to co-building, 2026-06-26) and the Herbarium's read-only per-resident pattern.
