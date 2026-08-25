---
name: joey-workflow
description: "Run Joey's reusable AI-cinematic production workflow as a persistent production map, analogous to Wayfinder for filmmaking. Start from a loose film, series, music-video, commercial, or cinematic-world idea; define the destination; build and approve canonical assets in dependency order; keep candidates separate from canon; and advance one human-approved frontier item at a time. Orchestrates story-bible-builder, character-builder, banana-pro-director-3.0, and cinema-director."
---

# Joey Workflow

A reusable workflow for producing a coherent AI-cinematic world across many sessions.

A loose cinematic idea is not yet a production. The path from idea to coherent footage passes through a chain of canonical decisions: world, characters, identities, outfits, props, locations, scene plates, motion, sound, and edit. Joey Workflow makes that chain explicit as a **shared production map** and advances it one approved asset at a time.

This skill is domain-agnostic. It can drive a documentary, narrative short, music video, commercial, episodic world, or experimental film. Project-specific canon belongs in the project's story-bible skill or files, never in this workflow skill.

## Build canon, not random outputs

The goal is not to generate many attractive images. The goal is to create a small, traceable set of **approved canonical assets** that downstream generations can depend on.

Every generated result is one of:

- **Candidate** — generated for review; not safe as a reference yet
- **Approved** — selected by the human as canonical
- **Rejected** — retained only as failure knowledge; never reused as reference
- **Superseded** — once canonical, now replaced by a newer approved asset

The agent never promotes a candidate to Approved on its own.

## One frontier item at a time

Work one unresolved canonical decision at a time. Do not silently continue from face lock to outfit, from outfit to sheet, or from scene plate to video.

After generating or drafting a candidate:

1. present it for review
2. wait for the human to approve, revise, or reject it
3. record the decision
4. only then expose the next dependent frontier item

Research or non-creative validation tasks may run in parallel when they cannot make or pre-empt a creative decision.

## Specialist skills

Joey Workflow orchestrates specialists; it does not replace their prompt grammar.

- **World and canon:** `story-bible-builder`
- **Character identity and wardrobe design:** `character-builder`
- **Still-image asset prompts:** `banana-pro-director-3.0`
- **Motion and video prompts:** `cinema-director`

When a project-specific story-bible skill is installed, load it as the canon source.

---

# The Production Map

Each project has one canonical production map. Store it in the project's own workspace or tracker. If no tracker or project location exists, default to:

```text
.joey/PRODUCTION_MAP.md
```

The map is an index and state machine, not a place to duplicate full prompts or bible content. Link to assets and source files rather than pasting all of them into the map.

Use the template in `references/production-map-template.md`.

## Map sections

- **Destination** — what completed production package or film this map is finding its way to
- **Canon source** — story bible and project rules
- **Pipeline** — stages enabled for this project
- **Approved canon** — approved assets and their identifiers
- **Frontier** — currently actionable items whose dependencies are approved
- **Blocked** — known items waiting on dependencies
- **Decisions** — concise record of approvals and production choices
- **Rejected directions** — drift patterns and candidates that must not return
- **Not yet specified** — in-scope fog that cannot yet be expressed as a precise item
- **Out of scope** — consciously excluded work

## Production items

Each production item resolves one canonical question and should fit in one focused session.

```markdown
## Item
<descriptive name>

## Canonical question
<exact decision this item must resolve>

## Stage
<bible | character | face-lock | outfit | character-sheet | prop | environment | scene-plate | video | audio | edit>

## Dependencies
<approved asset names or none>

## Inputs
<references, specifications, or canon sources>

## Acceptance criteria
<what the human must be able to approve>

## Status
<specified | candidate | approved | rejected | superseded>
```

Refer to items by descriptive name, not bare ids.

---

# The Canonical Pipeline

The pipeline is dependency-driven. Some projects omit stages, but no downstream item may be canonical before its actual dependencies are canonical.

## Stage 1 — Story Bible

Define the world before generating assets.

Lock, at minimum:

- premise and destination
- thesis or emotional question
- reality level and genre
- timeline or eras
- aesthetic rules
- locations
- characters and relationships
- recurring story engines
- production rules

Use `story-bible-builder` for the full interview and bible artifact.

**Gate:** the human approves the story bible or explicitly approves a minimal bible sufficient for a prototype.

## Stage 2 — Character text lock

Build one character at a time. Lock:

- function in the story
- face and body structure
- skin, hair, eyes, and identity markers
- movement and stillness patterns
- expression and emotional register
- voice and speech pattern when relevant
- prohibited drift

Use `character-builder`.

**Gate:** the human confirms the textual character specification.

## Stage 3 — Face lock

For a new photoreal character, the first image is an identity asset, not a scene.

Use Mode 0 from `banana-pro-director-3.0`:

- mid-gray seamless
- simple locked baseline wardrobe
- controlled neutral light
- identity-first framing
- no environment or narrative styling

Each output is a Candidate until the human explicitly selects it.

**Gate:** one face lock becomes Approved.

## Stage 4 — Base outfit

Build one full outfit reference on the approved identity.

- one outfit or story phase per item
- studio-readable styling
- accessories and hair state explicitly locked
- no character sheet before this base exists

Use `character-builder` and Mode 1 from `banana-pro-director-3.0`.

**Gate:** one base outfit image becomes Approved.

## Stage 5 — Character sheet

Build only from an approved face lock and approved base outfit.

Default to the Joey three-panel sheet:

1. headless full-body front outfit read
2. full-body rear with head attached
3. tight chest-up face lock

Six-panel is explicit-request only.

**Gate:** the sheet is approved as a continuity reference.

## Stage 6 — Props

Create canonical references for recurring or continuity-sensitive objects.

Examples: instruments, documents, phones, weapons, vehicles, bags, badges, mobility aids, product packaging, distinctive furniture.

**Gate:** recurring props that affect the first scene are Approved.

## Stage 7 — Empty environments

Build locations without characters before staging scenes in them.

Lock:

- architecture and geography
- time of day and weather range
- practical light sources
- material palette
- recurring set dressing
- camera-accessible spatial relationships

**Gate:** the required environment plate is Approved.

## Stage 8 — Scene plates

Combine approved references:

- face lock
- outfit or character sheet
- props
- environment
- story beat

A scene plate establishes composition, staging, light, and continuity before motion. Use Mode 3 from `banana-pro-director-3.0`.

**Gate:** the human approves a start frame, end frame, or visual scene anchor.

## Stage 9 — Video

Only now use `cinema-director` to convert the approved scene logic into motion.

Lock:

- shot purpose
- duration and capture cadence
- subject and wardrobe locks
- movement and stillness
- camera path
- environmental motion
- cross-frame continuity rules
- sound bed
- last frame

**Gate:** the video prompt is approved before rendering; rendered takes remain Candidates until selected.

## Stage 10 — Audio and edit

When applicable, define:

- dialogue and lipsync source
- diegetic sound
- music identity
- edit rhythm
- transitions
- color and grain continuity
- final disclosure or provenance rules

Only selected takes enter the canonical edit.

---

# Frontier rules

The **frontier** is the set of precise, unblocked production items that can be worked now.

An item enters the frontier only when:

- its canonical question is precise
- all required dependencies are Approved
- it does not force a decision that belongs to a later stage

Do not pre-slice the whole film into hundreds of rigid items. Keep uncertain future work in **Not yet specified**. Resolve the nearest canonical decision, then update the map as new details become visible.

## Human decision boundary

The human chooses among creative alternatives.

The agent may:

- explain differences
- identify continuity risks
- recommend a default
- generate revised candidates

The agent may not:

- select a face, costume, composition, performance, or edit without approval
- close a prototype item because one option looks strongest
- reinterpret silence as approval

---

# Invocation

Joey Workflow is explicitly invoked, like Wayfinder.

## Chart a production

Use when the user has a loose cinematic idea or an existing concept without a production map.

1. **Name the destination.** Define what the completed effort should produce: teaser, short, sequence, pilot, world package, music video, or full film.
2. **Locate the canon.** Find or create the story bible. Record which specialist and project skills apply.
3. **Map the first frontier.** Add only the precise canonical decisions visible now. Keep later uncertainty in Not yet specified.
4. **Wire dependencies.** Face lock blocks outfit; outfit blocks sheet; required props and environment block scene plate; scene plate blocks video.
5. **Choose the first item.** Usually the bible or first character specification.
6. Stop after charting unless the user explicitly asked to begin the first item in the same session.

## Continue a production

Use when the user provides a production map, project folder, or clear reference to an existing Joey project.

1. Load the low-resolution map and canon source.
2. Inspect the frontier, not every downstream item.
3. Choose one frontier item; prefer the user's named item, otherwise the earliest dependency.
4. Invoke the correct specialist skill.
5. Produce one candidate or decision package.
6. Wait for explicit human approval.
7. Record the result and recalculate the frontier.

## Review a candidate

When the user supplies a generated image, video, audio take, or prompt result:

1. identify which production item it belongs to
2. compare it against its acceptance criteria and canon locks
3. list concrete continuity matches and failures
4. ask the human to approve, revise, or reject
5. never promote it automatically

## Revise canon

When an approved asset changes:

1. mark the old asset Superseded, never silently overwrite history
2. identify all downstream assets that depend on it
3. reopen only those whose continuity is materially affected
4. preserve unaffected decisions

---

# Output behavior

At every step, state compactly:

- **Current item**
- **Why it is on the frontier**
- **Inputs and references required**
- **What approval will unlock next**

Before any expensive prompt, use the specialist skill's pre-prompt confirmation rule.

After a candidate is created, stop at the decision boundary. Do not proceed merely because the next step is obvious.

---

# Project adapters

Project-specific skills may supply canon, tone, constraints, characters, or disclosure rules. They plug into Joey Workflow through the Production Map's **Canon source** and **Notes**.

Examples:

- a documentary-world bible
- a music-video artist bible
- an episodic-series canon
- a brand or product visual bible

The adapter never changes the generic order or human approval boundary unless the project's Notes explicitly record an override.
