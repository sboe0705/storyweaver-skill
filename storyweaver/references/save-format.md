# Save Format

A save is a folder with two files:

```
storyweaver-saves/
└── <story-slug>/          # lowercase-hyphenated title, e.g. the-clockwork-heir
    ├── state.md           # for the next AI session
    └── story.md           # for human readers
```

Pick the slug once, when the story first gets saved, and keep it. Later saves overwrite `state.md` and add to `story.md`. If a folder with that slug already belongs to a different story, add a number to the new slug (`-2`).

## Contents

1. state.md: the resume file
2. story.md: the readable story
3. Chapters
4. Rewinds and branches

---

## 1. state.md: the resume file

This file has one job: a new session that has never seen the conversation should be able to continue the story without contradicting anything. When in doubt, include more. Use this template, and leave out sections that don't apply:

```markdown
<!-- STORYWEAVER SAVE — contains spoilers. Load with the storyweaver skill to continue. -->
# Save: <Story Title>

- **Format version:** 1
- **Saved at:** turn <N>, chapter <N> ("<chapter title>")
- **Readable story:** story.md

## Settings
- Genre / setting:
- Audience & tone:
- Length target: short | medium | epic (≈ <N> turns, currently at <N>)
- Puzzle difficulty:
- Language:
- Narrative voice used in story.md: e.g. third person, past tense, protagonist "Mara"
- User preferences noticed: e.g. "loves dialogue", "dislikes combat", "solves ciphers fast"

## Protagonist
Name, appearance, background, personality, and current condition.

## Hidden plan (spoilers)
- Central conflict and the truth behind it:
- Planned endings and what leads to each:
- Secrets not yet revealed:
- Upcoming planned beats / puzzles:

## Characters
| Name | Role | Motive / secret | Attitude to protagonist | Status / location |
|---|---|---|---|---|

## World state
Locations visited, doors opened, events triggered, time of day, deadlines, factions.

## Inventory
- item: where it came from, any special properties

## Clues & knowledge
- clue: where it was found, what it actually means (spoiler)

## Puzzles
| Puzzle | Status | Answer | Hints given |
|---|---|---|---|
| Riddle of the iron door | solved | "an echo" | 1 |
| Diary cipher | open | "BENEATH THE BELL" (Caesar +3) | 0 |

## Decision log
1. Turn 2: spared the smuggler → owes the protagonist a favor (not yet used)
2. ...

## Current scene
The last narration, shown in full, and the choices that were offered, shown word for word, so the next session can pick up right where the story stopped.
```

## 2. story.md: the readable story

This is the story as a reader would want it: polished prose, not a transcript of the game.

```markdown
# <Story Title>

*<one-line tagline or genre note>*

## Chapter 1: <Title>

<prose>

## Chapter 2: <Title>

<prose>

---

*The End.*    ← only once an ending has been reached
```

Writing rules:

- **Rewrite, don't copy.** Turn the in-game narration into connected prose. The user's decisions become things the protagonist does, and free-text actions are worked into the narrative. Leave out numbered choices, status lines, hints, wrong guesses (unless they make a nice moment), meta commands and out-of-character talk.
- **Voice:** By default, use third person, past tense and the protagonist's name, because that reads most like a novella. If the user prefers second person, or the story is clearly told in first person, use that instead. Whatever you choose, record it in `state.md` and keep it the same throughout.
- **Puzzles in the prose:** tell how the protagonist worked out the answer, so a reader can enjoy the solution without having played.
- **Length:** you may expand a little (add a transition, a description, a line of dialogue the scene implied), but don't invent events that didn't happen in play. The story should stay true to what the user actually decided.
- **Audience and language:** keep the audience, tone and language of the session.
- **Updating:** append new chapters. Rewrite only the chapter that is still in progress, because finished chapters are settled. Don't regenerate the whole file on every save.
- **Ending:** after the final chapter, add a short epilogue if one was played, then *The End.*

## 3. Chapters

Start a new chapter at a natural break: a change of location, a major revelation, a solved key puzzle, the end of an act, or a jump in time. A rough guide is one chapter every 3–6 turns. Short stories usually have 3–5 chapters, medium ones 6–10, and epics as many as they need. Give each chapter an evocative title that doesn't give the plot away.

A save in the middle of a chapter writes that chapter as it stands so far. Mark it with `<!-- in progress -->` under the heading, and remove the marker once the chapter is finished.

## 4. Rewinds and branches

If the user rewinds to an earlier decision, the abandoned path is no longer part of the story:

- In `story.md`, remove or rewrite the passages that came after the rewind point, so the readable story follows only the path that was actually kept.
- In `state.md`, restore the state as it was at that point. Keep a single line in the decision log, such as "Rewound from turn 12 to turn 8 (tried: opened the vault)", so the next session knows what the user has already seen.
