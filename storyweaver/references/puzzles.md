# Puzzle Catalog

A toolbox of puzzle types for interactive stories. Pick types that fit the genre, the scene, and the chosen difficulty. Vary them — three riddles in a row get stale.

## Contents

1. Design checklist
2. Puzzle types
3. Difficulty scaling
4. Multi-scene puzzles
5. Common mistakes

## 1. Design checklist

Before presenting a puzzle, confirm:

- [ ] The answer is fixed in your mind.
- [ ] All necessary information is in the story (now or earlier).
- [ ] The puzzle has an in-world reason to exist (who built the lock, who wrote the cipher, why?).
- [ ] Solving it moves the story forward or rewards the user (access, item, secret, ally).
- [ ] There are 2–3 hint steps prepared.
- [ ] There is a fallback if the user gives up.

## 2. Puzzle types

### Riddles
Classic word riddles, spoken by a guardian, carved on a door, sung in a song.
- Easy: "What has keys but can't open locks?" (a piano)
- Hard: original riddles tied to the story's lore — the answer is a character or place the user has encountered.
- Tip: Original riddles that reference the story are more satisfying than famous ones the user may already know.

### Ciphers and codes
Caesar shifts, symbol substitution, acrostics (first letters of lines), number-to-letter (A=1), hidden words in a text.
- Always give the key or a way to derive it (a shift number scratched on the wall, a symbol legend in another room).
- Keep the encoded message short (1–5 words).

### Combination locks
Numbers or symbols derived from clues: a date in a diary, the count of statues in the hall, a clock stuck at a specific time.
- Spread the digits across the scene or several scenes.

### Logic and deduction
Who is lying? Which door leads out? Ordering puzzles (five portraits, who sat where).
- State constraints clearly; ambiguity is the enemy here.
- For mysteries: physical evidence + testimony + motive → culprit.

### Observation
The answer is hidden in the scene description itself: a detail that doesn't fit, an object mentioned in passing.
- Be fair: mention the detail plainly, just not conspicuously. Don't hide it in deliberately vague language.

### Item combination and use
Use or combine inventory items: oil on the rusty hinge, a mirror to redirect light, rope + hook.
- Track inventory carefully; reward clever alternative solutions that make physical sense.

### Social puzzles
Persuading, bribing, tricking, or befriending a character. The "solution" is understanding what the character wants or fears.
- Seed their motive earlier in the story.

### Pattern and sequence
Musical notes, colored tiles, constellations, number sequences.
- Great for kids (colors, shapes) and scalable for adults.

### Environmental / spatial
Mazes described in text, levers and water levels, rotating rooms.
- Keep text-based spatial puzzles simple; complex geometry is hard to convey in prose. Offer a short summary of the current state each turn.

### Moral dilemmas
No single correct answer — the "puzzle" is a decision with costs either way. These don't need hints; they need consequences.

## 3. Difficulty scaling

| Difficulty | Steps to solve | Clue placement | Hints |
|---|---|---|---|
| Kids | 1 | Right in the scene, emphasized | Offered proactively after one wrong try |
| Easy | 1 | Same scene | On request or after 2 wrong tries |
| Medium | 1–2 | Same or previous scene | On request |
| Hard | 2–4 | Spread across several scenes | On request only, first hint is subtle |

## 4. Multi-scene puzzles

On medium/hard, a meta-puzzle that spans the story is very satisfying: fragments of a map, four seals for four locks, letters collected one by one to form a final password. Track collected pieces in the status line so the user sees progress.

## 5. Common mistakes

- **Moon logic** — solutions that make sense only to the author. Ask: would a reasonable person get there from the clues?
- **Moving the goalposts** — changing the answer after a guess. Never do this.
- **Pixel hunting in prose** — clues so buried the user must interrogate every noun.
- **Puzzle as filler** — a puzzle that doesn't connect to the plot. Every puzzle should reveal, unlock, or cost something.
- **Being too literal** — rejecting a correct answer phrased differently.
