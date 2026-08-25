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

Use Weaver Candidate A as:

- `STYLE REFERENCE` for Shots 01–24;
- `IDENTITY REFERENCE` for the Weaver in Shots 01–05 and 24 only;
- `WARDROBE REFERENCE` for the Weaver in Shots 01–05 and 24 only;
- `ENVIRONMENT REFERENCE` for the Weaver's room in Shots 01–05 and 24 only;
- `PROP REFERENCE` for the Weaver's loom in Shots 01–05 and 24 only.

Do not copy the Weaver's identity, clothing, room or loom into Shots 06–23 unless a later explicit human decision changes the role map.

### Weaver Candidate B

Weaver Candidate B is an unselected reference.

It has no active reference role in Still Pass 01.

It is not Rejected. Do not use it unless the production map records a new human decision.

### Generated continuity anchors

When `prompts/STILL_PASS_01.md` names a previous shot as a reference:

- use that shot only for the roles stated in the prompt;
- preserve the named identity, location, wardrobe, prop or state;
- do not infer additional canonical roles from the image.

## Continuity groups

| Group | Shots | Required continuity |
|---|---|---|
| Weaver and Child | 01–05, 24 | Weaver identity, Child identity, clothing, loom, room, thread |
| Coastal archive | 06–08, 18, 23 | two people, clothing, stone archive, shelf geometry, stored materials |
| Language record | 10, 17, 22 | elder, younger relative, room, recording equipment |
| Returned textile | 11, 13 | exact textile fragment and physical state |
| Return community | 12, 14–16, 21 | guardian, community members, cultural house, returned textile |
| Standalone climate and trade images | 09, 19, 20 | project visual DNA only unless the prompt defines another dependency |

## Still Pass 01 execution contract

`GOAL: Create one complete 24-frame storyboard Candidate set for contact-sheet review.`

`SCOPE: prompts/STILL_PASS_01.md inside the Higgsfield Cinema Studio festival project.`

`DECISION OWNER: HUMAN`

1. Generate the images in the recorded dependency order.
2. Use 16:9 landscape output.
3. Preserve every prompt and Higgsfield generation identifier.
4. Keep every output in Candidate state.
5. Complete all 24 technically usable frames.
6. Review the 24 frames in one 6 × 4 contact sheet.

The agent MUST NOT regenerate a creatively disappointing frame before the first complete review.

The agent MAY regenerate a frame before the review only when the output is technically unusable. Record the failed generation and the reason.

The first pass MAY use 24 generations.

The remaining 75 generations are a correction reserve. Do not spend the reserve before the contact-sheet decision.

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
- the requested action would use the correction reserve before contact-sheet review.

Report the exact blocked shot, unknown and required human decision.
