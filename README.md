# Storyweaver

An AI skill that turns Claude into a narrator and game master for **interactive stories of any genre** — with meaningful decisions, riddles and puzzles, and multiple endings.

## Features

- **Any genre** — fantasy, sci-fi, mystery, horror, adventure, romance, historical, fairy tales, comedy, or any mix.
- **Real choices** — 2–4 distinct options per turn plus free input; decisions are remembered and pay off later.
- **Fair puzzles** — riddles, ciphers, combination locks, deduction, item use, social puzzles; woven into the plot, with escalating hints so you never get stuck.
- **Adapts to you** — audience (kids to adults), tone, length and difficulty are configurable.
- **Meta commands** — `hint`, `inventory`, `recap`, `rewind`, `save` (portable save summary to continue in a new chat).
- **Multiple endings** — replay to discover different outcomes.

## Structure

```
storyweaver/
├── SKILL.md              # Core instructions: setup, turn format, choices, puzzles, pacing
└── references/
    ├── puzzles.md        # Puzzle catalog, fairness checklist, difficulty scaling
    └── genres.md         # Genre-specific storytelling toolkits
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
