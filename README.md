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

**Claude.ai / Claude Desktop**: download `storyweaver.zip` from the [latest release](https://github.com/sboe0705/storyweaver-skill/releases/latest) and upload it under *Settings → Capabilities → Skills*.

**Claude Code**: copy the skill folder into your skills directory:

```bash
cp -r storyweaver ~/.claude/skills/
```

## Building and releasing

```bash
./build.sh               # check the skill and write dist/storyweaver.zip
./build.sh --check-only  # only run the checks
./release.sh             # suggest the next version, tag it, and push the tag
./release.sh --dry-run   # show what a release would do
```

`build.sh` checks the `SKILL.md` frontmatter (name, description length) and makes sure that every `references/…` file the skill mentions exists. Then it packages the skill, with the LICENSE, into a reproducible zip.

GitHub Actions:
- **Build** (`.github/workflows/build.yml`) runs on every push to `main` and on every pull request. It checks the scripts, builds the zip, and uploads it as a workflow artifact.
- **Release** (`.github/workflows/release.yml`) runs when a `v*` tag is pushed, e.g. by `release.sh`. It builds the zip and publishes it as a GitHub release with generated notes.

## Usage

Just ask for a story, for example:

- "Let's play an interactive mystery set on a 1920s train."
- "Tell my 7-year-old a bedtime story where she gets to choose what happens."
- "I want a hard sci-fi adventure with lots of puzzles."
- "Surprise me!"

## License

[Apache License 2.0](LICENSE)
