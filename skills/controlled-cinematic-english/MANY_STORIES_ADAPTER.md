# Many Stories Adapter for Controlled Cinematic English

## Authority

This adapter contains stable rules for the **Many Stories** production.

The canonical live production state is `.joey/PRODUCTION_MAP.md`.

Before cinematic work:

1. Read `README.md`.
2. Read `.joey/PRODUCTION_MAP.md`.
3. Load Agent Technical English.
4. Load Controlled Cinematic English.
5. Load this adapter.
6. Load Joey Workflow.
7. Read only the stage sources named by the current frontier.
8. Load the specialist skill or the existing project prompt contract.

A current explicit human decision has authority over an older repository mirror. Record that decision in the production map before downstream reuse.

If `README.md`, the production map, the story bible, the screenplay or a prompt package conflict, stop the affected action. Report the conflict. Do not infer approval or choose a replacement.

## Layer responsibilities

- **Agent Technical English** controls agent instructions, tool procedures and handoffs.
- **Controlled Cinematic English** normalizes cinematic intent, reference roles, continuity and creative decision ownership.
- **Joey Workflow** controls production dependencies, asset status and approval gates.
- **Banana Pro Director** or the existing still-prompt contract controls still-image prompt grammar.
- **Cinema Director** controls motion and video prompt grammar.
- **The Higgsfield model adapter** maps the final prompt to the selected model and project surface.

CCE MUST NOT replace or rename a downstream specialist's prompt grammar.

## Stateless image-model contract

Nano Banana has no memory of an earlier shot, prompt, reference or visual rule.

For every shot package in `prompts/STILL_PASS_01.md`:

1. List every image that the operator MUST attach.
2. State one canonical role for each property taken from each reference.
3. Provide one self-contained prompt that the operator can copy without another text block.
4. Provide result-handling instructions outside the model prompt.

The prompt MUST contain every required textual visual rule.

The prompt MUST refer only to images that the operator attaches for that shot.

The prompt MUST NOT tell Nano Banana to preserve an output for a future shot.

Result handling MUST state:

- how to save and record the output;
- which continuity properties to verify;
- whether the output can serve as a provisional reference;
- which dependent shots must stop if the output is technically unusable.

A future dependency is an operator instruction. It is not a model instruction.


## Creative contract

The film is a cinematic allegory based on the PNyX “Global Treaty for Cultural Heritage.”

The film is not:

- a policy explainer;
- a PNyX product demonstration;
- archival reporting;
- a claim that the depicted people, practices or events are real.

The emotional movement is:

`inheritance → fragility → return → care → plurality`

The film MUST preserve this thesis:

> Humanity does not need one shared story. Humanity needs a shared way to protect many living stories without taking ownership away from the people who carry them.

The closing line is:

> The world does not gain a single story. It gains a way to protect its many stories.

## Decision authority

`DECISION OWNER: HUMAN`

The agent MAY:

- normalize intent;
- identify ambiguity;
- identify continuity risk;
- prepare Candidates;
- recommend a correction.

The agent MUST NOT:

- promote a Candidate to Approved;
- select a face, composition, cultural representation or final frame;
- reinterpret silence as approval;
- spend the correction reserve without a recorded frontier decision;
- convert a temporary prototype reference into permanent canon.

## Active reference-role map

### Weaver Candidate A

Attach Weaver Candidate A as an image reference for Group A (`A01`–`A06`) only.

Use it as:

- `STYLE REFERENCE` for Group A (`A01`–`A06`);
- `IDENTITY REFERENCE` for the Weaver in Shots 01–05 and 24;
- `WARDROBE REFERENCE` for the Weaver in Shots 01–05 and 24;
- `ENVIRONMENT REFERENCE` for the Weaver's room in Shots 01–05 and 24;
- `PROP REFERENCE` for the Weaver's loom in Shots 01–05 and 24.

For Groups B–H, use the shared textual visual DNA in `prompts/STILL_PASS_01.md`. Do not attach Weaver Candidate A. Do not copy the Weaver's identity, clothing, room, loom, rustic material palette or social context into unrelated communities.

### Weaver Candidate B

Weaver Candidate B is an unselected reference.

It has no active reference role in Still Pass 01.

It is not Rejected. Do not use it unless the production map records a new human decision.

### Generated continuity anchors

Still Pass 01 has an explicit in-pass Candidate-reference exception.

When `prompts/STILL_PASS_01.md` names a shot coordinate as a reference:

- use that Candidate only inside Still Pass 01;
- use it only for the roles stated in the reference-role matrix and prompt;
- preserve the named identity, location, wardrobe, prop or state;
- do not infer additional canonical roles from the image;
- do not promote the referenced Candidate to Approved;
- if the anchor is replaced, reopen each dependent shot whose continuity changes materially.

## Two-dimensional shot coordinates

The letter identifies the continuity group. The two-digit number identifies the local shot position inside that group. Use the coordinate for generation files, reference attachments and result handling. Preserve the film-shot number only as edit-order metadata.

| Group | Coordinates | Film shots | Required continuity |
|---|---|---|---|
| Weaver and Child | A01–A06 | 01, 02, 03, 04, 05, 24 | Weaver identity, Child identity, clothing, loom, room, thread |
| Coastal archive | B01–B05 | 06, 07, 08, 18, 23 | two people, clothing, stone archive, shelf geometry, stored materials |
| Dryland threshold | C01 | 09 | standalone project visual DNA |
| Language record | D01–D03 | 10, 17, 22 | elder, younger relative, room, recording equipment |
| Returned textile | E01–E02 | 11, 13 | exact textile fragment and physical state |
| Return community | F01–F05 | 12, 14, 15, 16, 21 | guardian, community members, cultural house, returned textile |
| Moving threshold | G01 | 19 | standalone project visual DNA |
| Trade | H01 | 20 | standalone project visual DNA |

The coastal archive, language-record household and return community MUST use the distinct visual systems defined in `.joey/STORY_BIBLE.md`. `C01` and `G01` MUST remain separate from those recurring communities.

## Still Pass 01 execution contract

`GOAL: Create one complete 24-frame storyboard Candidate set for contact-sheet review.`

`SCOPE: prompts/STILL_PASS_01.md inside the Higgsfield Cinema Studio festival project.`

`DECISION OWNER: HUMAN`

1. Generate each group from left to right. Generate the groups from A through H.
2. Use 16:9 landscape output.
3. Use exact image expansion for `A01`. If expansion is unavailable inside the festival project, stop `A01`.
4. Attach Weaver Candidate A only for Group A (`A01`–`A06`).
5. Use the self-contained prompt for each shot. For Groups B–H, the prompt contains the shared textual visual DNA and uses no Weaver image input.
6. For each shot, attach only the references listed in the runbook.
7. Preserve every prompt and Higgsfield generation identifier.
8. Keep every output in Candidate state.
9. Complete all 24 technically usable frames.
10. Review the 24 frames in one 6 × 4 contact sheet.

The agent MUST NOT regenerate a creatively disappointing frame before the first complete review.

The agent MAY regenerate a frame before the review only when the output is technically unusable. Record the failed generation and the reason.

The base pass MAY use 24 generations.

Technical failures MAY use at most 8 additional generations before review.

The remaining 67 generations are a creative correction reserve. Do not spend this reserve before the contact-sheet decision.

`DONE WHEN: Yiannis can mark every frame Keep, Repair or Replace while viewing the complete sequence.`

## Cultural representation contract

The agent MUST:

- represent people as capable participants;
- preserve contemporary life around inherited practices;
- keep different communities visually distinct;
- show community agency when knowledge is recorded, returned, relocated or shared;
- use ordinary contemporary clothing unless canon specifies otherwise.

The agent MUST NOT:

- invent or recreate a sacred ceremony;
- combine recognizable motifs from unrelated cultures;
- use generalized “tribal” styling;
- turn cultural difference into travel advertising;
- use generic poverty as visual shorthand;
- show a community as frozen in the past;
- make recorded knowledge appear ownerless.

## Festival and provenance rules

- Create all new image and video generations inside the Higgsfield Cinema Studio festival project.
- Use only fictional people who do not resemble identifiable real people.
- Generate all final audio with AI.
- Preserve prompts, project files and generation history for 24 months.
- Do not generate visible text, flags, logos, watermarks or readable interfaces unless a later deterministic compositing contract permits them.
- Do not present synthetic footage as archival evidence.

## Stop conditions

Stop the affected generation when:

- a required reference is missing;
- a reference role is ambiguous;
- two source files conflict;
- a prompt requires an unrecorded material creative choice;
- a generated anchor changes identity, wardrobe, location or prop geometry materially;
- a cultural representation risks combining unrelated or sacred material;
- `A01` requires ordinary regeneration instead of exact in-project image expansion;
- a prompt for Groups B–H would attach Weaver Candidate A;
- the requested action would use the creative correction reserve before contact-sheet review;
- more than eight technical-retry generations would be required before review.

Report the exact blocked shot coordinate, unknown and required human decision.
