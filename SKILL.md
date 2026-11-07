---
name: storyboard-previs-sheet
description: Create a director's previs storyboard sheet from screenplay beats and character reference images, especially monochrome early-stage boards with colored production annotations.
---

# Storyboard Previs Sheet

Create a readable storyboard sheet or a continuous multi-page storyboard that communicates framing, blocking, action, and camera progression. Use the image-generation tool for the image; do not substitute a textual shot list when an image is requested. Panel count is determined by the source shot prompts and the page's readability, never by a fixed default.

## Workflow

1. Read the requested scene, beat list, and any timing. If the user gives source text, preserve its story facts, dialogue constraints, character identities, and continuity.
2. Find and inspect the best available character reference image in the project. Pass it as a reference image to generation. Name or map the characters in the prompt. Keep faces, costume silhouette, age, and injuries consistent. If no reference image exists, ask for one only when likeness is central; otherwise proceed with a clearly described character.
3. Parse the source into shot IDs, durations, explicit cuts, camera changes, action beats, and important reactions before choosing a panel count. Make a panel plan in chronological order:
   - Use a new panel for every explicit cut to a new image, angle, shot size, or location.
   - For a continuous shot with no cut, use one panel when its composition remains readable and stable. Add panels for meaningful changes in framing, blocking, action phase, character reaction, or start/end state; identify these as keyframes from the same continuous shot, not extra cuts.
   - Do not make a panel for every second or every minor gesture. Preserve only visually meaningful changes, but do not omit a source cut, essential action phase, reaction, or continuity state to hit a target count.
   - Let panel count follow this plan. Twelve panels is only one possible layout, not a target or limit.
   - Split the sequence across as many sheets as needed for legible drawings and captions. Choose the grid and panel size for the material; do not shrink panels or text to force everything onto one page. Keep chronology intact and never drop excess beats.
   - Number panels continuously across pages and label each with source shot ID and time range. Give every page a page number and sequence range. At a page break, repeat or state the outgoing/incoming pose, screen direction, camera axis, location, and any held prop or injury needed to make the continuation unambiguous. Do not imply an edit where the source specifies a continuous shot.
   - Make time progression coherent; the final panel must show the requested end state.
4. Describe drawings as rough, lightweight previs: bold pencil contours, sparse hatching, simplified anatomy, clear silhouettes, limited background detail. Unless requested otherwise, keep all artwork itself strictly black and white. If the user asks for colored annotations, confine color to arrows, brackets, framing marks, or margin legends; explicitly distinguish annotation colors from drawing colors.
5. Make camera changes legible: state shot size or lens character, camera movement, screen direction, and any important axis/eyeline continuity. Use simple production marks for character motion, camera motion, composition, light, and vocal/emotional emphasis when requested. Include concise panel numbers and legible short captions; avoid dense explanatory prose inside panels.
6. Generate the planned sheet or page sequence. Inspect that every planned panel appears in order, shot IDs and time ranges are represented, page numbering and cross-page continuity are clear, and drawings, captions, identities, grayscale constraints, annotation colors, and key start/end states are readable. Check that no beats were omitted or duplicated and that panels have not been compressed to meet an arbitrary count. If a core requirement visibly failed, make one targeted regeneration or edit. Do not claim exact generated typography if the image has obvious text errors.
7. Save the image to the project only when the user asks for a project artifact or the task context clearly expects one. Preserve the original generated image and copy it into the requested project output folder. Report the saved path and any material visual limitation.

## Prompt construction

Specify the page format and planned number of pages/panels first, then reference-image role mapping, ordered visual beats with source shot IDs and time ranges, camera path, character blocking and end pose, monochrome drawing constraint, annotation-color legend, and typography. State that each explicit source cut gets its own panel; keyframes within a continuous shot are labeled as such. If more than one page is needed, specify continuous numbering, page sequence ranges, and the exact visual handoff at each page break. Choose a legible grid for each page instead of forcing a fixed 12-panel layout. Repeat the key negative constraint in plain language: color marks are overlays only; no color in the storyboard drawing. Do not ask the model to put a four-view character sheet into the page as a layout; use it only to anchor identity.

When the source is a timed video-generation prompt, treat its explicit timeline and cut instructions as authoritative. Do not infer that a single prompt equals a single storyboard panel or that a duration implies a fixed number of panels. Where a continuous shot needs multiple keyframes, use useful coverage of source-supported changes (establishing, closer composition, reaction, insert, end pose) and preserve chronology. Where the source does not support enough distinct moments for a requested count, do not invent beats merely to fill cells. Do not add dialogue, people, props, injuries, cuts, or events absent from the source.

For a monochrome-only request, omit colored annotations. Follow the requested aspect ratio and drawing style, while choosing panel count and page count from the planned coverage and legibility. If the user explicitly requests a fixed number of panels, honor it only when it can contain all required beats legibly; otherwise explain the constraint and split into multiple sheets while preserving the requested panel size and all source events.
