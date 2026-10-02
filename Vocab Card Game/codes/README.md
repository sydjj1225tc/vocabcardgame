# Reusable vocabulary card

Open `index.html` directly in a browser. It contains CSS, JavaScript, and an embedded image, and works offline without dependencies or external services.

With the project preview server running, visit http://127.0.0.1:8000/codes/.

## Review the code

1. **Presentation:** CSS positions and sizes each text area over the approved artwork.
2. **Content:** HTML creates the card and four editable text elements.
3. **Card data:** change the word, score, part of speech, definition, source, and image description here.
4. **Display:** JavaScript fills the text fields and removes a final period.
5. **Fit longer text:** reduces text size when needed. Always visually review new cards.
6. **Embedded art:** the long encoded line is image data; skip it when learning the code.
7. **Start:** displays the card and responds to changes in browser width.

`assets/morality-background.png` is the text-free artwork used in this template. The image is also embedded in the HTML for portability. Replacing the asset file alone does not update the embedded copy.

Follow `design-rules.md` for every future card. The earlier game prototype remains in the parent folder; this folder is the approved reusable card design.

## The four variables

Edit `powerPoints`, `image`, `partOfSpeech`, and `definition` in the `card` object. The word title is editable too. For a new word, supply a new illustration matching its meaning, with the same character and visual style. See `design-rules.md` for the image canvas and placement requirements. The fixed frame and variable central illustration are separate display layers.

## Grade 9 collection

Open `collection.html` to view value, obtain, and differ together. Each also has a standalone offline HTML file and an exported `WORD-card.png`. Editable word data is near the top of each HTML script; `cards-data.json` is a review copy, not a live data source. See `difficulty-notes.md` for the 10–150 point rubric, selected meanings, and Oxford sources. Full illustration prompts are in `grade9-image-prompts.md`.

## Rarity previews

Open `rarity.html` for the same differ card in all three tiers. In `collection.html`, use the selector above each card. Standalone cards also have a selector. Rarity changes only the frame treatment and panel tint, not the word, illustration or power points.

URL examples: `differ.html?rarity=rare` or `differ.html?rarity=unique`. Add `&export=1` to hide the control for an image export. Normal is the default; `embedded=1` hides duplicate controls inside the gallery. Choices reset on reload unless included in the URL.

The alternate frames were generated using the built-in image tool, saved in `assets/frame-rare.png` and `assets/frame-unique.png`, and embedded in each HTML for offline use. Only the frame outside the illustration cutout is displayed; the original word-specific illustration remains unchanged.
