# Vocab Card Game

An English vocabulary card collection project for US students in grades 7–12, currently focused on ninth grade.

**[Open the website](https://sydjj1225tc.github.io/vocabcardgame/)**

## Publishing

GitHub Pages publishes this repository from the root of `main`. Pushing changes to `main` triggers the Pages build and deployment. The root `index.html` opens the card collection; `.nojekyll` serves the standalone HTML and assets directly.

## View locally

Open `Vocab Card Game/codes/collection.html` in a browser. Cards work offline.

For a local preview:

```sh
cd "Vocab Card Game"
python3 -m http.server 8000 --bind 127.0.0.1
```

Visit http://127.0.0.1:8000/codes/collection.html.

- `Vocab Card Game/codes/`: card implementations, artwork, PNG exports, and rarity previews
- `Vocab Card Game/index.html`: original study-and-recall game prototype
- `Vocab Card Game/learning-notes.md`: beginner-friendly code explanations
- `AGENTS.md`: project collaboration and design rules

See the README files in the project and codes folders for details. Definitions are based on Oxford Learner’s Dictionaries; source references and scoring rationale are included in the project notes.

## Reflection

- What matched your intention, and what didn’t?

The basic elements of a word—the definition, part of speech, and power points—were in place, but the image generation was random. For example, Codex included another human character that destroys the premise of a world of sprites.

- What did you test or change, and why?

I asked Codex to change the details of the layout for consistency. Also, I asked it to delete the human character to match the lore of the game.

- How did AI help, and what did you need to decide or understand yourself?

Codex helped me visualize the concept design I had in mind. I evaluated its layout and components for accuracy as well as quality. It’s crucial that the human has a clear vision as well as each actionable step in mind.

- What remains uncertain or unresolved?

I still need to research which AI image generation tool is the most suitable for image generation that matches the definition. I want to better understand its machine learning process and the essential part of prompting to get the desired result.
