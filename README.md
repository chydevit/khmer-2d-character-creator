# Khmer 2D Character Creator & Consistency System

A Claude Code skill for designing **new original 2D cartoon characters** with a Cambodian / Khmer look,
for stories, folklore, history, motivational and kids' educational videos. The designs stay consistent
from scene to scene.

## Two styles
| Style A: Warm story (default) | Style B: Bright chibi |
|---|---|
| ![Style A](reference/master-style-sheet.png) | ![Style B](reference/style-b-bright-sheet.png) |
| Dara, Malis, Lok Ta Sokha, Veasna, Princess Bopha, King Jayavuth, Rotha + animals | bright 3-head chibi kids |

## What it does
- asks for name, role, age, personality, costume, colors and props
- writes a **character bible**: face, hair, body, clothing, hex palette, accessories (with which side),
  8–12 expressions, 6–10 poses
- writes an **IDENTITY LOCK**, the list of things that must never change
- writes a ready-to-paste **image prompt** (turnaround + expressions + action poses) and a **negative prompt**
- runs a 13-point **quality check** on the images you generate
- keeps cast lineups at the correct heights

## Files
```
SKILL.md                      the skill (rules + workflow)
reference/master-style-sheet.png   Style A master sheet
reference/style-b-bright-sheet.png Style B sheet
references/cast-bible.md      locked details of the 10 Style A sheet characters + height ladder
references/templates.md       role templates, generator format, prompt templates, negative prompt
examples/characters/          blank template + two examples:
    mother-sophea/  (Style A, Dara's mother, rice farmer)
    pisey/          (Style B, 7-year-old kite flyer)
```

## Install
Copy this folder to `.claude/skills/khmer-2d-character-creator/` in your project (or `~/.claude/skills/`),
then ask Claude Code something like *"create a new character: a fisherman grandfather, Style A"*.
In your project, new characters go in `characters/<name>/` (see `examples/characters/README.md`).

Companion skill for turning characters into films: [create-animation-2d](https://github.com/chydevit/create-animation-2d).
