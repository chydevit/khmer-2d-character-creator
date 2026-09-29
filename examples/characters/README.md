# New characters

Original characters made with the `khmer-2d-character-creator` skill, in the world of the master sheet
(`.claude/skills/khmer-2d-character-creator/reference/master-style-sheet.png`).

One folder per character, named in lowercase (for example `characters/srey-pov/`):

| File | What it holds |
|---|---|
| `<name>.md` | character profile + IDENTITY LOCK (copy `_template/character.md`) |
| `prompt.txt` | the final image-generation prompt + negative prompt |
| `sheet.png` | the APPROVED character sheet (front / 3/4 / side / back, expressions, poses) |
| `drafts/` | generated attempts that are not approved yet |
| `voice.wav` + `voice.txt` | optional: the locked VoxCPM2 reference clip + its exact transcript |

A folder that has `sheet.png` is **locked**. Never redesign that character without an explicit instruction from the user.
The 10 characters already on the master sheet are locked in the skill's `references/cast-bible.md`, not here.
