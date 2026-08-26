# Many Stories — Stateless Still Pass 01 Operator Runbook

## Status

Create 24 storyboard Candidates. Nano Banana is stateless: every generation receives only the images attached for that shot and the prompt copied for that shot.

`DECISION OWNER: HUMAN`

No generated result becomes Approved before the complete contact-sheet review. A technically usable Candidate may serve as a provisional reference only where this runbook names it.

## Operator contract

For every shot:

1. Attach only the images listed under **References to attach**.
2. Copy only the code block under **Prompt to paste**.
3. Follow **Result handling** before starting a dependent shot.

MUST NOT assume that Nano Banana remembers an earlier prompt, image, person, room, object or visual rule.

MUST NOT attach Weaver Candidate A to Shots 06–23.

MUST NOT treat a future-shot dependency as a model instruction. Future dependencies belong only in **Result handling**.

- Create every image inside the Higgsfield Cinema Studio festival project.
- Select **16:9 landscape** for every generation.
- Generate one base image per shot.
- Preserve every exact prompt, original image, generation identifier and documented technical failure.
- If a technically usable result is creatively disappointing, keep it as a Candidate and continue to the complete contact-sheet review.
- If a result is technically unusable, record the failure and reason. Do not use that result as a reference. Use a technical retry only within the recorded budget.

## Execution order by continuity group

Run the groups and shots in this order:

`A: 01 → 03 → 02 → 04 → 05 → 24`

`B: 06 → 07 → 08 → 18 → 23`

`C: 09`

`D: 10 → 17 → 22`

`E: 11 → 13`

`F: 12 → 14 → 15 → 16 → 21`

`G: 19`

`H: 20`

Group F has one cross-group dependency: complete a technically usable Shot 13 before Shots 14 and 15.

## Group A — Weaver and Child

Build the Weaver room, lock the Child, complete the hand details, and return to the room for the closing frame.

### Shot 01 — THE ROOM REMEMBERS

#### 1. References to attach

- Attach **Weaver Candidate A** — IDENTITY REFERENCE for the Weaver; WARDROBE REFERENCE for the knit cap and patterned fleece; ENVIRONMENT REFERENCE for the room; PROP REFERENCE for the loom; STYLE REFERENCE for the observational image language.

#### 2. Prompt to paste

```text
OUTPUT MODE: Create a 16:9 image expansion/outpaint from the supplied Weaver reference image. Preserve every original source pixel unchanged. Generate only beyond the source-image borders. Do not substitute an ordinary reference-based regeneration. Preserve the elderly woman’s exact face, age, knit cap, patterned fleece, heavy working hands, loom and lived-in domestic interior. Extend the existing room naturally into a restrained medium-wide right-side documentary composition at eye level with a plausible 35 mm lens. Continue the same soft winter window light, low saturation, cool gray ambient light, warm maintained wood with ordinary use, tactile fiber and subtle natural film grain. The woman must not look at the camera. Preserve the existing condition of the room. Do not beautify, artificially distress, clean, rearrange or redesign it. Do not add text, logos, mystical light, staged emotion, extra fingers, duplicated hands or impossible loom parts. If 16:9 image expansion is not available inside the festival project, stop this shot and record it as Blocked. Do not generate a replacement composition.
```

#### 3. Result handling

- Download the original result as `01_<generation-id>.png`.
- Record Shot 01, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify exact source-pixel preservation, Weaver identity, wardrobe, room, loom and 16:9 expansion. If the tool regenerated the source instead of expanding it, record a technical failure and stop this group.
- If technically usable, make it available as a provisional reference for Shots 02, 03, 04 and 24.

### Shot 03 — AT THE THRESHOLD

#### 1. References to attach

- Attach **Weaver Candidate A** — IDENTITY and WARDROBE REFERENCE for the Weaver.
- Attach **Shot 01 Candidate** — ENVIRONMENT REFERENCE for the room; PROP REFERENCE for the loom; STYLE REFERENCE for framing and light.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use the supplied Weaver reference image for the Weaver's identity and wardrobe. Use the supplied Shot 01 reference image for the room, loom, light and observational image language. Preserve the same elderly woman at the same loom. Add one fictional child aged 10–12 standing quietly in the open interior doorway behind the loom. Give the child ordinary contemporary clothes in muted charcoal and faded blue. The child watches without smiling or posing. Keep the Child’s face and clothing specific and clearly visible. Frame from slightly behind the loom at eye level with a plausible 35 mm lens. Keep the Weaver focused on her work. Use soft winter daylight, low saturation, maintained aged wood, tactile fiber and subtle natural film grain. Do not make the child resemble a celebrity or identifiable real person. Do not use folklore costume, sentimental staging, text, logos, extra people, malformed hands or fantasy lighting.
```

#### 3. Result handling

- Download the original result as `03_<generation-id>.png`.
- Record Shot 03, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify Weaver continuity, room and loom continuity, and one clear Child identity in the locked muted clothing.
- If technically usable, make it available as a provisional Child reference for Shots 04, 05 and 24.

### Shot 02 — TENSION

#### 1. References to attach

- Attach **Weaver Candidate A** — IDENTITY and WARDROBE REFERENCE for the Weaver.
- Attach **Shot 01 Candidate** — PROP REFERENCE for the loom; ENVIRONMENT REFERENCE for the room; STYLE REFERENCE for framing, light and surface treatment.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use the supplied Weaver reference image for the Weaver's identity and wardrobe. Use the supplied Shot 01 reference image for the loom, room, light and observational image language. Show a close observational view of the same elderly woman’s hands guiding the wooden shuttle through the loom and maintaining tension in the gray natural thread. Preserve her patterned fleece sleeves, aged hands and the exact aged loom construction shown in the references. Do not add dirt or new damage. Use a physically plausible 50 mm close frame with enough context to understand the action. Use soft window light, low saturation, warm maintained wood with ordinary use, cool gray shadow and subtle natural film grain. The hands must perform one clear weaving action. Do not show her face. Do not create decorative fantasy thread, perfect commercial craft photography, extra fingers, duplicated tools, impossible thread paths, text, logos or watermarks.
```

#### 3. Result handling

- Download the original result as `02_<generation-id>.png`.
- Record Shot 02, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify one mechanically plausible weaving action, correct hands, sleeves, loom, shuttle and thread path.
- If technically usable, make it available as a provisional reference for Shot 05.

### Shot 04 — LISTENING

#### 1. References to attach

- Attach **Weaver Candidate A** — IDENTITY and WARDROBE REFERENCE for the Weaver.
- Attach **Shot 01 Candidate** — ENVIRONMENT, PROP and STYLE REFERENCE for the room, loom and light.
- Attach **Shot 03 Candidate** — IDENTITY and WARDROBE REFERENCE for the Child; COMPOSITION REFERENCE for the Child's scale in the room.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use the supplied Weaver reference image for the Weaver's identity and wardrobe. Use the supplied Shot 01 reference image for the room, loom and light. Use the supplied Shot 03 reference image for the Child's identity, wardrobe and scale. Preserve the same Weaver, Child, clothing, loom and room. Show the Child seated nearby and listening while the Weaver continues to work and speaks naturally without turning toward the camera. The moment must feel incidental, not staged as a formal lesson. Frame both people in a quiet eye-level medium-wide composition with a plausible 35 mm lens. Let the loom partially separate them while their attention connects them. Use soft window light, low saturation, cool gray ambient light, warm maintained wood with ordinary use and subtle film grain. Keep expressions restrained. Do not show exaggerated speaking, theatrical emotion, direct eye contact with camera, folklore costume, text, logos, duplicated people, extra fingers or impossible loom geometry.
```

#### 3. Result handling

- Download the original result as `04_<generation-id>.png`.
- Record Shot 04, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify both identities, both wardrobes, room, loom, eyelines and restrained incidental interaction.
- Do not promote the result to Approved. Continue only after the continuity checks pass.

### Shot 05 — THE LOOSE END

#### 1. References to attach

- Attach **Weaver Candidate A** — IDENTITY and WARDROBE REFERENCE for the Weaver.
- Attach **Shot 02 Candidate** — BODY REFERENCE for the Weaver's hands and sleeves; PROP REFERENCE for the loom, shuttle and thread.
- Attach **Shot 03 Candidate** — IDENTITY and WARDROBE REFERENCE for the Child.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use the supplied Weaver reference image for the Weaver's identity and wardrobe. Use the supplied Shot 02 reference image for her hands, sleeves, loom, shuttle and thread. Use the supplied Shot 03 reference image for the Child's identity and wardrobe. Preserve the same Weaver, Child, sleeves, hands, loom and thread. Show the Weaver placing the Child’s hand beside one loose gray thread at the edge of the unfinished cloth. The Child’s fingers hover and do not pull yet. Frame only the two sets of hands, part of the loom and a small glimpse of their bodies. Use a plausible 50 mm close documentary composition. Keep the action mechanically clear and emotionally restrained. Use soft natural window light, low saturation, warm maintained wood with ordinary use, tactile fiber and subtle film grain. Do not create hand-holding sentimentality, glowing thread, extra fingers, merged hands, duplicated thread, jewelry, text, logos or commercial craft styling.
```

#### 3. Result handling

- Download the original result as `05_<generation-id>.png`.
- Record Shot 05, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify both sets of hands, sleeve continuity, one loose thread and mechanically plausible contact with the loom.
- If technically usable, make it available as a provisional hands, thread and loom reference for Shot 24.

### Shot 24 — THE NEXT HANDS

#### 1. References to attach

- Attach **Weaver Candidate A** — IDENTITY and WARDROBE REFERENCE for the Weaver; ENVIRONMENT REFERENCE for the room; PROP REFERENCE for the loom.
- Attach **Shot 01 Candidate** — ENVIRONMENT and STYLE REFERENCE for the room, light and framing.
- Attach **Shot 03 Candidate** — IDENTITY and WARDROBE REFERENCE for the Child.
- Attach **Shot 05 Candidate** — BODY and PROP REFERENCE for hands, thread, shuttle and unfinished cloth.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use the supplied Weaver reference image for the Weaver's identity and wardrobe. Use the supplied Shot 01 reference image for the room, loom, light and observational image language. Use the supplied Shot 03 reference image for the Child's identity and wardrobe. Use the supplied Shot 05 reference image for the hands, thread, shuttle and unfinished cloth. Return to the same soft winter daylight. Show the Child now seated at the loom and operating the wooden shuttle carefully. The Weaver sits nearby in profile and watches without correcting every movement. The cloth remains visibly unfinished and several loose natural threads remain separate at its edge. Frame an eye-level medium-wide 35 mm composition with quiet breathing space. Use low saturation, cool gray ambient light, warm maintained wood with ordinary use, tactile fiber and subtle film grain. Do not show triumph, a staged smile, magical thread, perfect finished cloth, direct eye contact with camera, text, logos, extra fingers, duplicated hands or impossible loom geometry.
```

#### 3. Result handling

- Download the original result as `24_<generation-id>.png`.
- Record Shot 24, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify exact Weaver and Child continuity, room, loom, shuttle, unfinished cloth and separate loose threads; verify the ending remains quiet and unperformed.
- Keep the result as the closing-frame Candidate for contact-sheet review. Do not promote it to Approved.

## Group B — Coastal archive

Build one fictional coastal archive and reuse only its named people, clothing, architecture and archive state.

### Shot 06 — THE TIDE LINE

#### 1. References to attach

- Attach no image reference.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Show a small present-day coastal community archive built from maintained local stone and timber marked by salt exposure at gray high tide. Seawater has reached the entrance step but has not yet become a disaster spectacle. Establish one fictional older woman and one fictional young adult approaching the doorway with practical urgency. Use ordinary contemporary clothing suitable for damp coastal weather. Frame a calm eye-level wide shot with a plausible 35 mm lens. Use muted blue-gray daylight, maintained materials with ordinary age and subtle film grain. Avoid travel-advertising beauty, generic poverty, panic, flags, readable signs, logos, crowds, fantasy weather or recognizable real people.
```

#### 3. Result handling

- Download the original result as `06_<generation-id>.png`.
- Record Shot 06, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify that the people and archive are distinct from the Weaver group, contemporary, cared for and visually specific. If identity or location is unusable, record a technical failure and stop this group.
- If technically usable, make it the provisional coastal-archive anchor for Shots 07, 08, 18 and 23.

### Shot 07 — WATER INSIDE

#### 1. References to attach

- Attach **Shot 06 Candidate** — IDENTITY and WARDROBE REFERENCE for the older woman and young adult; ENVIRONMENT REFERENCE for the coastal archive.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 06 reference image for the exact coastal archive, older woman, young adult and clothing. Inside the same stone archive, show a thin layer of seawater crossing the floor while the two people lift plain archival boxes from a low shelf. Their action is coordinated and practical, not panicked. Frame an eye-level medium-wide view with a plausible 35 mm lens. Show paper boxes, folded cloth and simple recording media without readable labels. Use soft gray daylight from the doorway, low saturation, wet stone reflections, maintained timber with ordinary age and subtle film grain. Do not add flood spectacle, collapsing walls, rescue uniforms, dramatic hero poses, readable text, logos, duplicated boxes, malformed hands or impossible water behavior.
```

#### 3. Result handling

- Download the original result as `07_<generation-id>.png`.
- Record Shot 07, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same two people, clothing and archive; verify shallow plausible water, coordinated box handling and unreadable labels.
- If technically usable, make it available as a provisional archive-state and materials reference for Shots 08 and 18.

### Shot 08 — ABOVE THE WATER

#### 1. References to attach

- Attach **Shot 06 Candidate** — IDENTITY and WARDROBE REFERENCE for the two people; ENVIRONMENT REFERENCE for the archive.
- Attach **Shot 07 Candidate** — PROP REFERENCE for the boxes, cloth and recording media; ENVIRONMENT REFERENCE for the water level and archive response.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 06 reference image for the coastal archive, people and clothing. Use the supplied Shot 07 reference image for the boxes, cloth, recording media and water state. Show a close practical action: the older woman’s and young adult’s hands place one archival box, a small reel recorder, several photographs turned face-down and one folded cloth on the highest temporary wooden shelf. A thin layer of seawater remains visible far below. Use a plausible 50 mm close frame with clear shelf geometry. Use soft gray daylight, low saturation, tactile paper, cloth, oxidized metal, wet stone and subtle film grain. Do not show readable writing, visible photograph faces, sacred objects, panic, glowing water, extra fingers, duplicated items, text, logos or glossy disaster photography.
```

#### 3. Result handling

- Download the original result as `08_<generation-id>.png`.
- Record Shot 08, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same people, archive and materials; verify photographs are face-down, the shelf geometry is plausible and no text is readable.
- If technically usable, make it available as a provisional stored-materials reference for Shots 18 and 23.

### Shot 18 — A ROOM PREPARED FOR WATER

#### 1. References to attach

- Attach **Shot 06 Candidate** — IDENTITY and WARDROBE REFERENCE for the two people; ENVIRONMENT REFERENCE for the archive exterior and location.
- Attach **Shot 07 Candidate** — ENVIRONMENT REFERENCE for the archive interior and its water-entry condition.
- Attach **Shot 08 Candidate** — PROP REFERENCE for the stored materials and high-shelf organization.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 06 reference image for the exact coastal archive exterior, older woman, young adult and clothing. Use the supplied Shot 07 reference image for the archive interior after water entry. Use the supplied Shot 08 reference image for the stored materials and high-shelf organization. Show the same interior after practical adaptation: archival shelves are permanently raised above a floodable stone floor, boxes are orderly but not pristine, and simple ventilation openings are visible. The older woman and young adult inspect the room together after a small tide has receded. Frame an eye-level wide 35 mm shot that clearly explains the raised geometry. Use soft gray daylight, low saturation, damp stone, maintained timber with ordinary age and subtle film grain. Do not create a futuristic renovation, luxury design, disaster spectacle, readable labels, flags, logos, extra people, malformed architecture or impossible water reflections.
```

#### 3. Result handling

- Download the original result as `18_<generation-id>.png`.
- Record Shot 18, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same coastal people and archive; verify raised shelves, ventilation and floodable-floor geometry are physically plausible.
- If technically usable, make it available as a provisional adapted-interior reference for Shot 23.

### Shot 23 — THE HOUSE IS ALIVE

#### 1. References to attach

- Attach **Shot 06 Candidate** — IDENTITY and WARDROBE REFERENCE for the older woman and young adult; ENVIRONMENT REFERENCE for the coastal archive.
- Attach **Shot 08 Candidate** — PROP REFERENCE for the archival boxes, photographs and raised storage.
- Attach **Shot 18 Candidate** — ENVIRONMENT REFERENCE for the adapted raised-shelf interior and its dry operational condition.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 06 reference image for the exact coastal people, clothing and archive. Use the supplied Shot 08 reference image for the archival boxes, photographs and raised storage. Use the supplied Shot 18 reference image for the adapted raised-shelf interior. Show the room active in ordinary present-day life: two children look through reproduced photographs, the older woman speaks with another adult, and the young adult checks an archival box on a raised shelf. Keep all visible images and notes unreadable. Frame an eye-level wide 35 mm shot with several small actions but no crowd. Use soft late-afternoon daylight, slightly warmer skin tones, low saturation, stone and maintained timber with ordinary age and subtle film grain. Do not stage a festival, museum tour or classroom lesson. Do not show costumes, banners, text, logos, posing, duplicated people or malformed hands.
```

#### 3. Result handling

- Download the original result as `23_<generation-id>.png`.
- Record Shot 23, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same coastal people and adapted archive, dry and safe material handling, ordinary activity, unreadable images and no crowd.
- Keep the result as a Candidate for contact-sheet review. Do not promote it to Approved.

## Group C — Dryland threshold

Create one standalone fictional dryland community. Do not import continuity from another group.

### Shot 09 — SAND AT THE DOOR

#### 1. References to attach

- Attach no image reference.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Show two fictional residents clearing windblown sand from the carved wooden threshold of a modest present-day earth-built home at the edge of an increasingly dry landscape. Their clothing must be ordinary, practical and locally plausible without generalized ethnic or ceremonial styling. The threshold must appear maintained and still used, not presented as an archaeological ruin. Frame an eye-level medium-wide shot with a plausible 35 mm lens. Use pale overcast daylight, muted earth colors, maintained aged wood, fine dust and subtle natural film grain. Do not invent sacred symbols, combine unrelated cultural motifs, show exotic travel imagery, create a sandstorm spectacle, add text, flags, logos, extra limbs or recognizable real people.
```

#### 3. Result handling

- Download the original result as `09_<generation-id>.png`.
- Record Shot 09, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify a distinct fictional dryland community, an actively used threshold, ordinary contemporary clothing and no sacred or borrowed motifs.
- Keep the result as a standalone Candidate. Do not reuse its people or location in another continuity group.

## Group D — Language record

Build one inland household and preserve its people, room and locally controlled recording setup.

### Shot 10 — THE LAST FLUENT VOICE

#### 1. References to attach

- Attach no image reference.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. In a modest present-day kitchen, show one fictional elderly speaker talking quietly into a simple field microphone while one fictional younger adult relative listens with full attention. Keep both people, their clothing and the room specific and clearly visible. Place an old cassette recorder and a small notebook on the table, but show no readable writing. Frame an intimate eye-level two-person composition with a plausible 50 mm lens. Use soft side-window light, low saturation, ordinary wear and subtle film grain. The recording must feel consensual and community-owned, not extractive research. Do not use lab coats, outsider interviewers, staged smiles, costumes, text, logos, visible screen content, celebrity likenesses or exaggerated sadness.
```

#### 3. Result handling

- Download the original result as `10_<generation-id>.png`.
- Record Shot 10, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify a distinct elder, younger relative, clothing, kitchen and consent-centered recording setup. If identity or room is unusable, record a technical failure and stop this group.
- If technically usable, make it the provisional language-record anchor for Shots 17 and 22.

### Shot 17 — THE COMMUNITY RECORDS ITSELF

#### 1. References to attach

- Attach **Shot 10 Candidate** — IDENTITY and WARDROBE REFERENCE for the elder and younger relative; ENVIRONMENT REFERENCE for the kitchen; PROP REFERENCE for the recording setup.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 10 reference image for the exact elderly speaker, younger relative, clothing, kitchen and recording setup. Add one fictional local archivist of similar community context. Show the archivist operating a simple field recorder while the younger relative logs the session on a modest laptop with the screen turned away and unreadable. The elderly speaker talks naturally and remains in control of the exchange. Frame an intimate eye-level 35 mm three-person composition. Use soft side-window light, low saturation, ordinary domestic wear and subtle film grain. Do not show an outsider research team, surveillance, studio glamour, staged smiles, readable notes, screen content, logos, flags, extra equipment, duplicated people or celebrity likenesses.
```

#### 3. Result handling

- Download the original result as `17_<generation-id>.png`.
- Record Shot 17, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same elder, younger relative, clothing and kitchen; verify the archivist belongs to the same fictional community and all screens are unreadable.
- If technically usable, make it available as a provisional locally controlled recording reference for Shot 22.

### Shot 22 — A LIVING VOICE

#### 1. References to attach

- Attach **Shot 10 Candidate** — IDENTITY and WARDROBE REFERENCE for the elder and younger relative; ENVIRONMENT REFERENCE for the room.
- Attach **Shot 17 Candidate** — PROP REFERENCE for the locally controlled recording equipment; COMPOSITION REFERENCE for the locally controlled session.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 10 reference image for the exact elderly speaker, younger relative, clothing and room. Use the supplied Shot 17 reference image for the locally controlled recording equipment and session. In the same modest room, show the younger relative using a small contemporary sampler or audio workstation with the screen turned away while the elder listens. The younger person is creating something new from the recorded voice with the elder present and attentive. Frame an intimate eye-level 35 mm two-person composition. Use soft natural light, low saturation, ordinary cables and equipment, lived-in surfaces and subtle film grain. Do not turn the scene into a nightclub, commercial music studio or sentimental performance. Do not show readable interfaces, logos, headphones as fashion styling, celebrity likenesses, staged smiles or extra people.
```

#### 3. Result handling

- Download the original result as `22_<generation-id>.png`.
- Record Shot 22, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same elder and younger relative, the same modest room, ordinary contemporary equipment and an unreadable interface.
- Keep the result as a Candidate for contact-sheet review. Do not promote it to Approved.

## Group E — Museum textile

Build the exact textile fragment, then preserve its physical design during packing.

### Shot 11 — BEHIND GLASS

#### 1. References to attach

- Attach no image reference.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity, tactile fiber and subtle natural film grain. Show one old handwoven textile fragment lying alone inside a sterile metropolitan museum display case. Give it an invented asymmetric field of charcoal and faded-rust bands crossed by small irregular cream rectangles, with one frayed lower corner and two visible repaired seams. The textile must appear handmade, aged, carefully preserved and specific but must not copy sacred or recognizable cultural motifs. Place blurred visitors and polished architecture far behind the glass. Use a restrained eye-level 50 mm composition with the empty space around the textile dominating the frame. Contrast cool institutional light with the warm fibers. Add subtle natural film grain. Do not show readable labels, museum names, dramatic spotlights, treasure glamour, fantasy patterns, reflections that create fake people, text, logos or watermarks.
```

#### 3. Result handling

- Download the original result as `11_<generation-id>.png`.
- Record Shot 11, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the exact asymmetric charcoal, faded-rust and cream textile pattern, the frayed lower corner and two repaired seams. If the textile is not reusable as an exact prop reference, record a technical failure and stop the museum-textile group.
- If technically usable, make it the provisional exact-textile reference for Shot 13.

### Shot 13 — PACKING THE RETURN

#### 1. References to attach

- Attach **Shot 11 Candidate** — PROP REFERENCE for the exact textile fragment and its physical state; ENVIRONMENT REFERENCE for the museum context.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 11 reference image for the exact textile fragment, its physical state and the museum environment. Show a conservator carefully placing the same textile into an archival transport crate with neutral tissue and support material. The conservator’s action must be professional and restrained. Frame a clear 50 mm close documentary view of hands, textile and crate. Keep the crate label side outside the frame. Use cool institutional daylight, low saturation, tactile fiber, plain wood and subtle film grain. Do not turn the return into a heroic gesture. Do not show readable paperwork, museum branding, white-glove glamour, extra fingers, duplicated textile, impossible folds, text, logos or watermarks.
```

#### 3. Result handling

- Download the original result as `13_<generation-id>.png`.
- Record Shot 13, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify exact textile continuity, professional handling, neutral support material and a crate with no readable label.
- If technically usable, make it the provisional textile-and-crate reference for Shots 14 and 15.

## Group F — Return community

Build one return community and cultural house. Shot 13 from Group E is also required before Shots 14 and 15.

### Shot 12 — THE EMPTY PLACE

#### 1. References to attach

- Attach no image reference.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. In a modest present-day community cultural house, show one fictional middle-aged community guardian touching the edge of a clean, deliberately empty mounting place between two related contemporary community-made textiles on a limewashed wall. Include two quietly present community members. Keep the guardian, the room and both community members specific and clearly visible. Their clothing must be ordinary and contemporary. Frame an eye-level medium-wide 35 mm shot with the empty wall space clearly visible. Use soft natural daylight, low saturation, maintained timber with ordinary age, earth plaster and subtle film grain. The scene must express absence without theatrical grief. Do not show a flag, invented traditional costume, sacred ceremony, readable text, logos, staged crying, crowds or recognizable real people.
```

#### 3. Result handling

- Download the original result as `12_<generation-id>.png`.
- Record Shot 12, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify a distinct return-community guardian, two community members, the cultural house and the clean empty mounting place. If identity or room is unusable, record a technical failure and stop the return-community group.
- If technically usable, make it the provisional return-community anchor for Shots 14, 15, 16 and 21.

### Shot 14 — ARRIVAL

#### 1. References to attach

- Attach **Shot 12 Candidate** — IDENTITY and WARDROBE REFERENCE for the guardian and community members; ENVIRONMENT REFERENCE for the cultural house.
- Attach **Shot 13 Candidate** — PROP REFERENCE for the closed transport crate and its scale.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 12 reference image for the exact community guardian, other people and cultural-house environment. Use the supplied Shot 13 reference image for the closed transport crate. Show the same community members receiving the closed crate through the ordinary entrance of their modest cultural house. They move it together with a small practical trolley. No official delegation is present. Frame an eye-level medium-wide 35 mm shot with a visible threshold and quiet physical effort. Use soft natural daylight, low saturation, maintained timber with ordinary age, stone, plain crate wood and subtle film grain. Do not show flags, banners, applause, press cameras, uniforms, ceremonial costume, readable labels, logos, staged celebration, extra people or malformed hands.
```

#### 3. Result handling

- Download the original result as `14_<generation-id>.png`.
- Record Shot 14, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify return-community identity, clothing and room continuity; verify the crate remains closed and the trolley action is plausible.
- If technically usable, make it available as a provisional crate-scale and arrival-state reference for Shot 15.

### Shot 15 — OPENING

#### 1. References to attach

- Attach **Shot 12 Candidate** — IDENTITY and WARDROBE REFERENCE for the guardian and community members; ENVIRONMENT REFERENCE for the cultural house.
- Attach **Shot 13 Candidate** — PROP REFERENCE for the exact textile fragment and protective material.
- Attach **Shot 14 Candidate** — PROP and COMPOSITION REFERENCE for the crate and its scale in the room.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 12 reference image for the exact community people and room. Use the supplied Shot 13 reference image for the textile. Use the supplied Shot 14 reference image for the crate and its scale in the room. Show the open crate on a sturdy worktable as the community guardian and two other members see the returned textile for the first time. Keep their expressions quiet, concentrated and complex. One person may rest a hand on the table, but nobody touches the textile yet. Frame an eye-level medium-wide 35 mm shot with the textile visible inside protective material. Use soft window light, low saturation, tactile cloth, paper, wood and subtle film grain. Do not show cheering, staged tears, officials, sacred performance, readable text, flags, logos, extra fingers or duplicated people.
```

#### 3. Result handling

- Download the original result as `15_<generation-id>.png`.
- Record Shot 15, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same three people, room, crate and exact textile; nobody touches the textile.
- If technically usable, make it available as a provisional returned-textile state reference for Shot 16.

### Shot 16 — LEARNING AGAIN

#### 1. References to attach

- Attach **Shot 12 Candidate** — IDENTITY and WARDROBE REFERENCE for the guardian and two community members; ENVIRONMENT REFERENCE for the cultural house.
- Attach **Shot 15 Candidate** — PROP REFERENCE for the returned textile and its opened-return physical state.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 12 reference image for the exact community guardian, other members and room. Use the supplied Shot 15 reference image for the returned textile and opened-return state. Show the guardian seated beside two fictional young adult weavers. The returned textile rests safely on the worktable while the younger people begin a new small sample on a simple loom. They study structure, not copy a tourist pattern. Frame an eye-level medium-wide 35 mm composition that includes both generations, the old textile and the new unfinished work. Use soft natural daylight, low saturation, warm maintained wood with ordinary use, tactile fiber and subtle film grain. Keep clothing contemporary and gestures unperformed. Do not create ceremonial costume, cultural collage, commercial workshop imagery, glowing patterns, text, logos, malformed hands or impossible loom mechanics.
```

#### 3. Result handling

- Download the original result as `16_<generation-id>.png`.
- Record Shot 16, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same guardian and two young weavers, the exact returned textile, a separate new sample and plausible loom mechanics.
- If technically usable, make it available as a provisional young-weaver and working-material reference for Shot 21.

### Shot 21 — THE REPAIR

#### 1. References to attach

- Attach **Shot 12 Candidate** — IDENTITY and WARDROBE REFERENCE for the return-community members; ENVIRONMENT REFERENCE for the cultural house.
- Attach **Shot 16 Candidate** — IDENTITY REFERENCE for the young weavers; PROP REFERENCE for their working materials.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Use the supplied Shot 12 reference image for the exact return-community cultural house, guardian and community members. Use the supplied Shot 16 reference image for the young weavers and their working materials. Show the same modest workshop receiving practical conservation materials: untreated timber, archival boxes, humidity tools and rolls of neutral cloth. The community members inspect and organize the supplies themselves. No donor representative appears. Frame an eye-level medium-wide 35 mm shot with clear human action and ordinary physical effort. Use soft natural daylight, low saturation, warm maintained wood with ordinary use, paper, cloth and subtle film grain. Do not show gift-ceremony staging, oversized aid branding, readable labels, flags, logos, applause, luxury equipment, generic poverty, extra people or malformed hands.
```

#### 3. Result handling

- Download the original result as `21_<generation-id>.png`.
- Record Shot 21, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify the same return-community people and cultural house, practical materials, no donor representative and no readable labels.
- Keep the result as a Candidate for contact-sheet review. Do not promote it to Approved.

## Group G — Moving threshold

Create a second, standalone coastal community. Do not reuse the coastal-archive cast or location.

### Shot 19 — MOVING THE THRESHOLD

#### 1. References to attach

- Attach no image reference.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape observational-documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Show a fictional mainland coastal settlement with pale granite cottages, weathered slate roofs and ordinary contemporary navy or muted-orange rainwear. Show residents and conservation workers carefully relocating one aged but maintained carved wooden doorway from a small shoreline structure to a prepared safe foundation farther inland. Community members direct the action and workers use simple visible supports. The carving must be geometric and non-sacred without copying a recognizable culture. Frame an eye-level medium-wide 35 mm shot with the old shoreline visible in the distance and the new foundation in the foreground. Use muted coastal daylight, low saturation, maintained aged wood, stone and subtle film grain. Do not show a heroic rescue spectacle, heavy futuristic machinery, ceremonial costume, flags, readable signs, logos, impossible lifting, extra limbs or a collapsing building.
```

#### 3. Result handling

- Download the original result as `19_<generation-id>.png`.
- Record Shot 19, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify a different coastal community, a non-sacred geometric doorway, community-led direction and physically plausible supports.
- Keep the result as a standalone Candidate. Do not reuse its people or location for the coastal-archive group.

## Group H — Trade

Create one standalone auction image with no cultural-continuity dependency.

### Shot 20 — THE TRADE

#### 1. References to attach

- Attach no image reference.

#### 2. Prompt to paste

```text
Create one photoreal 16:9 landscape documentary still. Use raw observational-documentary realism, soft available daylight, restrained contrast, low saturation, a location-specific material palette, cared-for surfaces with ordinary use, candid gestures, quiet dignity and subtle natural film grain. Show a restrained international art auction room with affluent fictional bidders seated beneath one spotlit antiquity. Keep the object generic, non-sacred and partly obscured. Show no recognizable auction house. Frame from the back of the room at eye level with a plausible 50 mm lens. Let raised bidder paddles and tailored clothing suggest wealth, but keep all numbers and writing invisible. Use cool controlled light, low saturation and subtle film grain. The image must feel observational, not glamorous. Do not show brands, readable paddles, price displays, logos, celebrity likenesses, red-carpet styling, fantasy treasure, cultural collage or exaggerated villain expressions.
```

#### 3. Result handling

- Download the original result as `20_<generation-id>.png`.
- Record Shot 20, the exact prompt and the Higgsfield generation identifier.
- Keep the result in **Candidate** state. Do not mark it Approved.
- Verify a generic partly obscured object, unreadable paddles, no auction-house identity, no celebrity likeness and no glamorous villain framing.
- Keep the result as a standalone Candidate. Do not use it as a cultural-reference anchor.

## Completion gate

Create one 6 × 4 contact sheet after all 24 shots have technically usable Candidates.

`DONE WHEN: Yiannis can mark every frame Keep, Repair or Replace while viewing the complete sequence.`
