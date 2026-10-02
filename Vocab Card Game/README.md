# Vocab Card Game

A vocabulary-card prototype for US students in grades 7–12.

## Run

Open `index.html` directly in a browser. It works offline, with no dependencies or external services.

For a local preview, run from this folder:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Visit http://127.0.0.1:8000. Stop the server with Ctrl+C.

## Play

Study the card, select **Test your recall**, and choose the definition. A correct answer unlocks **Add to my collection**. Select **Practice again** to repeat. Collection progress resets on reload.

## Design

JavaScript generates a friendly golden compass using inline SVG. The mnemonic “morality → moral compass” connects the word to principles that guide right and wrong behavior. Honesty/care and cheating/harm provide concrete examples. The original vector art borrows the supplied cards’ gold frame, purple fantasy colors, sparkles, expressive mascot, noun badge, and meaning panel.

All CSS, JavaScript, and artwork are in `index.html`. The recall interaction hides the definition while retaining the visual cue. Controls support keyboard navigation and feedback uses a live status region.

## Read the code

Open `index.html` in an editor and follow the numbered comments:

1. **CSS — appearance:** change colors, spacing, and layout.
2. **HTML — content:** review the word, definition, prompts, and answer choices.
3. **JavaScript — behavior:** follow sections 3A–3F. For the learning sequence, start with 3B; the drawing coordinates in 3A are optional reading.

The code uses named variables, reusable functions, loops, conditions, and click events. See `learning-notes.md` for a short guide connecting these concepts to learning design.

## Approved reusable card design

Open `codes/index.html` for the illustrated card with editable HTML text and no period after the definition. See `codes/README.md` for its code guide and `codes/design-rules.md` for the design standard for all future cards.
