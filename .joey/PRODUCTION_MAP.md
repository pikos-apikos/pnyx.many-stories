# Joey Production Map

## Destination

Produce a coherent 3:20–3:50 AI short film titled **Many Stories** for the Higgsfield Global Film Festival. Build and review a complete 24-still storyboard before motion generation.

## Canon source

- Project brief: `README.md`
- Source concept: PNyx — “Global Treaty for Cultural Heritage”
- Candidate story bible: `.joey/STORY_BIBLE.md`
- Candidate screenplay: `SCREENPLAY.md`
- Still prompts: `prompts/STILL_PASS_01.md`
- Public workflow: `skills/joey-workflow/SKILL.md`
- Execution language: `skills/agent-technical-english/SKILL.md`
- Cinematic intent compiler: `skills/controlled-cinematic-english/SKILL.md`
- Project CCE adapter: `skills/controlled-cinematic-english/MANY_STORIES_ADAPTER.md`
- Skill loading manifest: `skills/manifest.yaml`
- Generation surface: Higgsfield Cinema Studio festival project

## Pipeline

- [ ] Minimal story bible — Candidate v0.2
- [ ] Character text locks — provisional inside Still Pass 01
- [ ] Face locks — provisional storyboard anchors only
- [ ] Base outfits
- [ ] Character sheets
- [ ] Props
- [ ] Empty environments
- [ ] Scene plates — 24 Candidates generated; human selection pending
- [ ] Video
- [ ] Audio / edit

## Approved canon

| Asset | Stage | Version | Location | Depends on |
|---|---|---:|---|---|
| Submission track: Create in public — 50 shortlist spots & production grants | production rule | 1 | `README.md` | none |
| Weaver Candidate A as temporary visual DNA | visual rule | 1 | `README.md` | none |

## Frontier

### Review Still Pass 01 contact sheet

- **Canonical question:** Does the complete 24-frame sequence form one coherent visual film?
- **Stage:** scene-plate prototype
- **Dependencies:** Twenty-four technically usable Still Pass 01 Candidates
- **Inputs:** `.joey/STORY_BIBLE.md`, `SCREENPLAY.md`, `prompts/STILL_PASS_01.md`
- **Acceptance criteria:** Yiannis records one Keep / Repair / Replace decision for each of the 24 Candidates while viewing the complete 6 × 4 sequence.
- **Status:** candidate
- **Decision owner:** HUMAN
- **Prototype exception:** The user explicitly authorized a complete Candidate pass before individual approval. No output becomes Approved through this exception.
- **In-pass reference exception:** A generated Candidate MAY be used as a provisional continuity anchor only inside Still Pass 01 and only for roles named in the prompt contract.
- **Invalidation rule:** Replacing a provisional anchor reopens each dependent shot whose continuity changes materially.
- **Generation budget:** 24 base generations, up to 8 technical-failure retries, and 67 creative correction generations held until contact-sheet review.

## Blocked

- Canonical story bible — blocked by the complete visual review.
- Approved scene plates — blocked by Keep / Repair / Replace decisions.
- Video prompts — blocked by approved scene plates.

## Decisions

- 2026-08-25 — Selected festival track: **Create in public — 50 shortlist spots & production grants**.
- 2026-08-25 — Selected Weaver Candidate A as the temporary visual DNA for Still Pass 01.
- 2026-08-25 — The first visual pass will cover the complete film before individual image approval.
- 2026-08-25 — Every output in the first visual pass remains a **Candidate**. The pass does not create approved canon.
- 2026-08-25 — Review the 24 Candidates together as one contact sheet.
- 2026-08-25 — Allocate 24 of the 99 free generations to the complete first pass, up to 8 to documented technical failures, and 67 to post-review continuity repairs, alternate compositions, missing inserts and final replacements.
- 2026-08-25 — Published Joey Workflow and Agent Technical English as reusable public skills in this repository.
- 2026-08-25 — Removed one obsolete unsupported Joey frontmatter key before public validation. The workflow instructions did not change.
- 2026-08-25 — Licensed the repository, reusable skills and production documentation under Apache-2.0.
- 2026-08-25 — Pinned Controlled Cinematic English and added a Many Stories project adapter plus deterministic loading manifest.
- 2026-08-25 — Yiannis delegated the Still Pass 01 correction-profile selection to the agent. Generated-image approval remains HUMAN.
- 2026-08-25 — `A01` (film shot 01) uses exact 16:9 image expansion. If expansion is unavailable inside the festival project, `A01` becomes Blocked.
- 2026-08-25 — Attach Weaver Candidate A only for Group A (`A01`–`A06`; film shots 01–05 and 24). Groups B–H use self-contained textual visual DNA and no Weaver image input.
- 2026-08-25 — Defined three visually distinct recurring fictional communities: coastal archive, language record and return community.
- 2026-08-25 — Use `prompts/STILL_PASS_01.md` as the authoritative still specialist contract for this prototype. Do not claim Banana Pro Director validation until that skill is pinned and run.
- 2026-08-26 — Restructured Still Pass 01 as a stateless Nano Banana operator runbook: continuity groups, explicit reference attachments and roles, self-contained copy/paste prompts, and per-shot result handling.
- 2026-08-26 — Adopted two-dimensional shot coordinates. The letter identifies the continuity group; the local two-digit number starts at 01 inside every group. Film-shot numbers remain edit-order metadata.

## Rejected directions

- Unrelated attractive images without a shared visual lock — they cannot establish film continuity.
- Automatic promotion of any first-pass image to Approved — the human owns all creative selections.
- Spending all 99 generations before the first contact-sheet review — it removes the correction budget.
- Generalized “traditional” or “tribal” styling — it collapses distinct communities into a cultural collage.
- Attaching Weaver Candidate A to Groups B–H — it can leak the Weaver, room and rustic materials into unrelated communities.
- Artificial grime or exaggerated distress — ordinary use must not become dirt, neglect or generic poverty.
- Fantasy thread, mystical glow or luxury travel imagery — it breaks the approved observational realism.

## Not yet specified

- Keep / Repair / Replace state for each of the 24 generated frames.
- Exact transition and insert needs after the first contact-sheet review.
- Final motion model and shot durations.
- Final narrator voice and sound design.

## Out of scope

- Generating outside the Higgsfield Cinema Studio festival project.
- Identifiable real-person likenesses or voices.
- Product-demo or policy-explainer treatment.
- Automatic creative approval by an agent.
