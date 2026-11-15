# Storyweaver

An AI skill that turns Claude into a narrator and game master for **interactive stories of any genre** — with meaningful decisions, riddles and puzzles, and multiple endings.

## Features

- **Any genre** — fantasy, sci-fi, mystery, horror, adventure, romance, historical, fairy tales, comedy, or any mix.
- **Real choices** — 2–4 distinct options per turn plus free input; decisions are remembered and pay off later.
- **Fair puzzles** — riddles, ciphers, combination locks, deduction, item use, social puzzles; woven into the plot, with escalating hints so you never get stuck.
- **Adapts to you** — audience (kids to adults), tone, length and difficulty are configurable.
- **Meta commands**: `hint`, `inventory`, `recap`, `rewind`, `save`.
- **Save files and a readable book.** Where Claude can write files, each save creates two files in `storyweaver-saves/<story>/`:
  - `state.md`: the full game state, so a new session can continue the story. Contains spoilers.
  - `story.md`: the story so far as polished prose in chapters. When you finish, it is a complete short story or novella.

  Both files also update automatically at the end of each chapter. Without file access, Claude prints the save as text for you to copy.
- **Multiple endings** — replay to discover different outcomes.

## Structure

```
storyweaver/
├── SKILL.md              # Core instructions: setup, turn format, choices, puzzles, pacing
└── references/
    ├── puzzles.md        # Puzzle catalog, fairness checklist, difficulty scaling
    ├── genres.md         # Genre-specific storytelling toolkits
    └── save-format.md    # Structure of state.md and story.md, chapter rules
```

## Installation

**Claude Code** — copy the skill folder into your skills directory:

```bash
cp -r storyweaver ~/.claude/skills/
```

**Claude.ai** — zip the `storyweaver` folder and upload it under *Settings → Capabilities → Skills*.

## Usage

Just ask for a story, for example:

- "Let's play an interactive mystery set on a 1920s train."
- "Tell my 7-year-old a bedtime story where she gets to choose what happens."
- "I want a hard sci-fi adventure with lots of puzzles."
- "Surprise me!"

## License

[Apache License 2.0](LICENSE)
