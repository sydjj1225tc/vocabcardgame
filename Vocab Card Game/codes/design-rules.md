# Approved card design

Use this design for all future cards in this project.

- Keep the identity reference's portrait layout, ornate gold frame, purple header, score shield, central illustration, gold part-of-speech plaque, pale definition panel, and book icon.
- Keep the approved ivory catlike character, expressive glossy eyes, purple rainbow-edged cloak, painterly shading, and magical lighting. Adapt the character's action and props to each word's mnemonic.
- Communicate the mnemonic through the illustration, without explanatory words in the scene.
- Put the part of speech on the gold plaque, in title case: Noun, Verb, Adjective, etc.
- Put only the definition in the definition panel. Do not repeat the part of speech. Do not add a period at the end.
- Always verify the definition and part of speech at https://www.oxfordlearnersdictionaries.com/us and save the entry URL and selected sense.
- Morality uses the noun entry, sense 1, verified September 22, 2026: https://www.oxfordlearnersdictionaries.com/us/definition/english/morality. The card retains US spelling “behavior” for US students; the source entry uses “behaviour”.
- Keep code simple, with explanatory comments for a learning designer with basic coding knowledge.

The background is a generated raster illustration, not a procedural JavaScript recreation. The HTML controls the layout and editable text. A future word needs a matching mnemonic illustration as well as updated card data; changing the word alone does not create new art.

## Reusable style versus variable content

The morality wallet scene is specific to morality. Never reuse it for an unrelated word. Keep only the character identity, style, and card layout consistent across the collection.

Each card has four content variables:
1. `powerPoints`: the numeric value in the upper-left shield
2. `image`: a new definition-specific scene using the established character and style
3. `partOfSpeech`: the Oxford-verified label in the lower middle plaque
4. `definition`: the Oxford-verified meaning, with no final period

The word title is also editable. The image description and dictionary source are supporting metadata.

The renderer separates the fixed frame from the variable illustration with a cutout. Image inputs use a 1024 × 1536 full-card coordinate canvas, with the scene in the same central area as the reference. Only that central scene is visible from the variable image; its border and text areas are ignored. This is a layout contract, not a requirement to reuse the morality scene. Image generation happens during card creation; the offline renderer does not generate a new illustration from text automatically.

## Updated rules: multiple meanings and character cast

- Include all numbered Oxford headword senses across the word's parts of speech. Label each definition with a number, starting each on a separate line. Distinguish parts of speech and usage restrictions. Idioms and separate compound headwords are not included automatically.
- Use concise source-based paraphrases when needed; label them as such in documentation. Preserve the meaning of each sense.
- All multi-definition words receive more than 100 points, up to 150. Current assignments: value 150, obtain 130, differ 110.
- Do not put slashes in definitions. Use “or” instead. No final periods.
- Keep the established guardian. Do not add unnecessary characters. The value card now uses the guardian alone.
- A longer definition list may need a larger pale text panel, rather than illegibly small text.

## Rarity colors

Increasing order: **Normal — purple; Rare — green; Unique — bright orange**. Rarity is independent of word difficulty and power points. Default to Normal; do not infer tiers from scores. Keep the central illustration and gold trim, changing the header, shield, lower border, and pale definition-panel tint. The sample image supplied September 22 is a color reference only.
