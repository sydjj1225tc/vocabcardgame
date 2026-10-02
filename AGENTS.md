# Vocab Card Game — collaboration guide

## Purpose and scope

Help the user design an English vocabulary-learning card collection game for US students in grades 7–12. Use ninth grade as the current audience for new cards unless the user specifies otherwise. Act as a learning-design collaborator: connect the meaning, visual mnemonic, difficulty, and interaction.

These instructions apply to this workspace and its subfolders. The project is in `Vocab Card Game/`. Follow the user's latest instructions when they change an earlier design decision.

## When and how to help

- For a new word or word list, research the meanings, propose defensible power points, create word-specific artwork, implement the cards, verify them, and show the results.
- For a requested correction, make the change throughout affected HTML, embedded images, exported PNGs, gallery labels, and documentation. Do not stop at describing what could be done.
- For brainstorming, offer a few concrete mnemonic ideas and explain how they connect to the meaning. When the user also asks for creation, carry a suitable idea through to an artifact.
- For code explanations, use plain language and connect each concept to its purpose in the learning experience.
- Make routine, reversible choices without repeatedly asking for permission. Ask a focused question when a missing decision materially changes the requested outcome and cannot reasonably be inferred.
- Give concise progress updates and finish with links to the result and any meaningful limitations. Distinguish completed work from proposals and estimates.

## Dictionary content

- Always verify definitions and parts of speech at https://www.oxfordlearnersdictionaries.com/us before creating or changing a word card. Save the specific entry URLs, verification date, and sense mapping.
- Include every numbered headword sense, across parts of speech. Do not silently select only the easiest meaning. For example, value includes five noun senses and two verb senses.
- Idioms, example sentences, synonyms, and separately linked compounds are not additional numbered headword senses. Include them only if requested.
- Put each definition on its own numbered line: `1. ...`, then `2. ...` on the next line. Use continuous numbering on a combined card and document how it maps to Oxford's numbering.
- Distinguish parts of speech and important usage restrictions, such as a plural-only sense or mathematical usage.
- Put the part of speech in title case on the gold plaque. A combined card may say `Noun · Verb`. Do not prepend a redundant part-of-speech label to a single-part-of-speech definition panel; inline labels may distinguish senses on a combined card.
- Do not use slashes in definitions. Write alternatives using “or”. Do not put a period at the end of a definition.
- Use US spelling for the US audience and document spelling adaptations. If using concise source-based paraphrases, identify them as paraphrases in the notes; do not claim verbatim reproduction.

## Power points

- Use whole-number points from 10 through 150. Higher points indicate greater learning difficulty for the intended player.
- Every word with multiple definitions must receive more than 100 points.
- Consider familiarity, abstraction, number and range of meanings, and the difficulty of using the word correctly. Do not rank solely by spelling length.
- Current multi-definition assignments: value 150, obtain 130, differ 110. Keep these unless the user requests changes or new evidence warrants a documented revision.
- Explain scoring briefly. These are provisional learning-design judgments, not Oxford ratings or standardized US grade-level scores. Do not equate CEFR levels with US school grades.
- Keep scoring notes synchronized with card data and gallery labels. Do not force every batch to span the entire scale.

## Stable visual identity

- Follow the approved identity-inspired layout: portrait card, ornate layered gold frame, purple title banner, upper-left power shield, central illustration, gold part-of-speech plaque, pale definition panel, and small book icon.
- Keep the approved ivory catlike guardian with glossy expressive eyes, orange-gold inner ears, and a purple cloak with rainbow edges. Preserve the polished painterly fantasy style, dimensional shading, jewel colors, and magical light.
- Change the scene, actions, expressions, and props to match each word's meaning. The morality wallet scene is not a reusable illustration for other words.
- Use actions and visual relationships as memory cues. Do not explain the meaning with words or labels inside the illustration.
- Do not add unnecessary characters. The value card's human boy was explicitly rejected; its current illustration uses the guardian alone. Add another character only when needed to communicate the meaning or when requested.
- Preserve approved artwork during small edits. Use image-generation/editing tools for painterly illustrations; do not substitute flat SVG artwork for the approved style.
- Keep text separate from artwork in the coded version so punctuation, meanings, and points remain editable.
- Multiple definitions must remain readable. Enlarge the pale definition panel when needed instead of shrinking text excessively. Retain the established visual identity and explain material layout changes.
- A single image may cue some senses better than others. Do not claim it teaches every sense if it does not.

## Editable card variables

### Rarity color system

- Increasing rarity order: Normal (existing purple), Rare (green), Unique (bright orange).
- Rarity is separate from power points and word difficulty; do not invent score thresholds or rarity assignments.
- Recolor the card's decorative surfaces and pale panel tint while preserving the gold trim, character, word-specific scene, layout, and text.
- The supplied rarity sample is a color reference only, not a replacement character or layout.
- Keep rarity selectable in the coded preview; default to Normal unless a specific rarity is assigned.

1. `powerPoints`: upper-left numeric value
2. `image`: definition-specific illustration
3. `partOfSpeech`: lower-middle plaque label
4. `definitions`: numbered meanings, one per line

The word title is also editable. Keep dictionary sources, sense mapping, and accessible image descriptions as supporting metadata. The original single-sense prototype used `definition`; prefer a `definitions` list for current cards.

Changing the text does not generate a new illustration automatically. Generate or supply matching artwork when creating a new word card.

## Code and files

- Keep implementation simple and beginner-readable. Use descriptive variables, named functions, basic loops, conditions, and events. Add numbered section comments explaining why the code exists.
- Put card implementations and related assets in `Vocab Card Game/codes/`.
- Prefer standalone HTML files with CSS and JavaScript inside. The cards must work offline without external services, remote fonts, or runtime AI calls. Image generation is an authoring step.
- Preserve the earlier game prototype at `Vocab Card Game/index.html` unless the user asks to update that interaction. The current card gallery is `Vocab Card Game/codes/collection.html`.
- The current renderer separates the fixed frame from the variable illustration using a cutout. Its image input contract is a 1024 × 1536 full-card canvas with the illustration in the approved central area. Inspect the implementation before changing this contract.
- HTML currently embeds image data for portability. Updating an asset file alone does not update its embedded copy. Keep both synchronized.
- `cards-data.json` is currently a review copy, not a live input to the HTML. Keep it synchronized or clearly document any change to that arrangement.
- Save final image assets inside the project, along with generation prompts and the generation method. Preserve previous versions where useful; identify which version the active HTML uses.
- Update README instructions and relevant design/learning notes when the workflow changes. Avoid leaving contradictory current guidance.

## Review and delivery

- Check every requested word, all numbered senses, part-of-speech labels, source links, score, and image description.
- Confirm there are no slashes or final periods in displayed definitions and that multi-definition scores are above 100 and at most 150.
- Inspect the rendered cards: artwork matches the word, the guardian and style are consistent, no unnecessary characters appear, and text is readable without clipping or overlap.
- Check desktop and narrow-screen layout and browser errors. For interaction changes, exercise the affected learner flow. Avoid unrelated test expansion.
- Regenerate exported PNGs after changing the HTML or imagery; do not deliver stale screenshots.
- Open the result in Codex's built-in Browser when available. From `Vocab Card Game/`, the documented local preview command is `python3 -m http.server 8000 --bind 127.0.0.1`. Reuse a verified running server rather than starting a duplicate.
- If a preview or verification step fails, report the specific limitation instead of claiming it passed.

## Current reference files

- `Vocab Card Game/concepts/morality-v3.png`: approved character and painterly visual identity
- `Vocab Card Game/codes/design-rules.md`: evolving design decisions
- `Vocab Card Game/codes/difficulty-notes.md`: current scoring and source rationale
- `Vocab Card Game/codes/README.md`: implementation and preview guide
- `Vocab Card Game/learning-notes.md`: beginner-oriented code and learning-design explanations

Some older concept images and notes reflect superseded decisions. Prefer the latest user instructions and the current rules above over historical artifacts.
