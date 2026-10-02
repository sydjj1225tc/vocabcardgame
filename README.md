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
