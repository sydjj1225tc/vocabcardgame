# Understanding the Vocab Card Game

The learning sequence is **study → recall → feedback → collect → practice again**.

## Three layers in one file

| Layer | Purpose | Example |
| --- | --- | --- |
| HTML | Learning content and structure | The definition and answer buttons |
| CSS | Visual presentation | The gold frame and mobile layout |
| JavaScript | Responses to learner actions | Check an answer and show feedback |

## Basic computational concepts

| Concept | Plain-language meaning | Use in this game |
| --- | --- | --- |
| Variable | A named place to keep a value | `hasCollectedCard` remembers whether the reward was earned |
| Boolean | A true-or-false value | `hidden = true` hides an element |
| Function | A reusable set of instructions | `startQuiz()` prepares a fresh recall attempt |
| Parameter | Information passed into a function | `checkAnswer(selectedButton)` receives the selected answer |
| Condition | A decision using `if` and `else` | A correct answer unlocks collection; another answer gives a hint |
| List and loop | A group of items and a repeated action | Reset every answer button before practice |
| Event | Something the learner or browser does | A button click runs its connected function |
| State | What the program currently remembers | Collection status persists during practice but resets on reload |

## Follow one answer

1. The learner clicks an answer button.
2. Its click event calls `checkAnswer`, passing that button.
3. The function reads the button's `data-correct` label from the HTML.
4. An `if/else` chooses confirmation or a corrective hint.
5. A correct answer reveals the collection button.
6. Collecting updates the counter and shows the transfer prompt.

The definition is hidden during recall, but the picture remains as a scaffold. The task is recognition from choices, not unaided recall. The final wallet prompt invites application; the prototype does not score that spoken answer.

## Safe editing exercises

- Change a prompt in section 2 (HTML), refresh, and inspect the result.
- Change a color in section 1 (CSS).
- Change a feedback sentence in `checkAnswer` (JavaScript).
- Add a coordinate pair to `starPositions` to draw another sparkle.

Keep exactly one answer marked `data-correct="true"`. Incorrect answers use `data-feedback` labels so their hints do not depend on their exact wording. If you change an incorrect answer's concept, update its hint too.

SVG artwork uses coordinates to describe shapes. You can understand and edit the learning interaction without learning every drawing command. All artwork is generated locally; no AI service runs when the page opens.

## Card design rules for future work

- Keep the approved ivory catlike guardian character, glossy eyes, rainbow-edged purple cloak, and painterly fantasy style from `concepts/morality-v3.png`.
- Match the identity reference card's layout.
- The gold plaque displays the word's part of speech (for example, **Noun**), not a conceptual category.
- The definition panel contains only the definition, without repeating the part of speech.
- Always verify definitions and parts of speech with https://www.oxfordlearnersdictionaries.com/us before making a card.
- Morality source: https://www.oxfordlearnersdictionaries.com/us/definition/english/morality — noun, sense 1. Verified September 22, 2026. This entry spells “behaviour”; the card uses US spelling “behavior” for the intended US students.
- Current approved-layout concept: `concepts/morality-v3.png`. The playable HTML prototype still uses the earlier SVG illustration.

## Latest approved design implementation

The reusable template is now `codes/index.html`. Follow `codes/design-rules.md` for all future card generations. The definition must have no terminal period. The illustration and frame are preserved as a raster background; the title, score, part of speech, and definition are editable HTML text. This replaces the earlier concept as the design reference for new cards.

## Rarity as a separate variable

The new `rarity` value can be `normal`, `rare`, or `unique`. A function called `setRarity` chooses the matching frame image and panel colors. It does not change `powerPoints` or the learning content. The selector demonstrates an event: changing the choice calls the function. The three tiers increase in rarity: purple, green, bright orange. This distinction lets the same word appear in different collectible editions without changing its difficulty.
