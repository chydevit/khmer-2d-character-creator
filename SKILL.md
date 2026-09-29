---
name: khmer-2d-character-creator
description: Khmer 2D Character Creator & Consistency System — design NEW original 2D cartoon characters (heroes, friends, mentors, warriors, princesses, kings, villains, farmers, monks, animals) that belong in the same animated world as the master style sheet (Dara the cream-shirt boy with red scarf, Malis, Lok Ta Sokha, Veasna, Princess Bopha, King Jayavuth, Rotha, the puppy, monkey and baby elephant). Produces character bibles, turnaround/expression/pose specs, identity locks, cast lineups and image-generation prompts for Khmer folklore, history, motivational, educational and kids' stories. Use whenever the user asks to create/design a new character, a character sheet or model sheet, a cast lineup, an image prompt for one of these characters, or to check a character for consistency — even if they don't name this skill. Two styles: A = the Dara master sheet (default), B = the bright chibi style of the green-shirt boy / golden-outfit girl sheet (new characters only; the boy and girl themselves belong to khmer-cartoon-characters).
---

# Khmer 2D Character Creator & Consistency System

**Purpose:** create original 2D cartoon characters for stories, educational and motivational videos,
Khmer folklore, historical animation, children's content and short films. Every new character must
look as if it came from the same animated world as the master sheet.

## Two styles: pick one per film, never mix them
| | **Style A: Warm story (default)** | **Style B: Bright chibi** |
|---|---|---|
| Sheet | `reference/master-style-sheet.png` | `reference/style-b-bright-sheet.png` |
| Look | warm cream/maroon/gold, painted cel shading, adventure & history | bright saturated colors, very clean white background, rounder chibi faces |
| Kids | ~4 heads tall, spiky/messy hair allowed | ~3 heads tall (head = 1/3 of height), neat simple hair |
| Height unit | Dara = 1.00 | green-shirt boy = 1.00 |
| Best for | folklore, history, motivational shorts | young children's lessons, songs, simple stories |

Default to Style A. Use Style B when the user asks for it or the film already uses it. Write `Style: A` or
`Style: B` at the top of every character file and prompt, and attach **that** style's sheet.
Style B rules: the green-shirt boy and golden-outfit girl on that sheet are locked in
`khmer-cartoon-characters` and are not copied here. New Style B characters must be clearly different
people (different hair, outfit colors and signature) but keep the same face construction, eye style,
line weight and proportions.

## 0. Before anything: look at the master sheet
`reference/master-style-sheet.png` (in this skill folder) is the **MASTER ART STYLE REFERENCE** for Style A
(`reference/style-b-bright-sheet.png` for Style B, and everything below applies the same way).
Read the image before designing, prompting or checking any character. When an image or video tool
accepts a reference image, attach this file.

- Do **not** copy a sheet character exactly unless the user asks for that character.
- New characters: same face construction, eye/nose/mouth style, line weight, shading, costume detailing.
- The locked cast from the sheet is in `references/cast-bible.md`. Read it when a story uses any of them.
- New characters live in the project folder `characters/<name>/` (see `characters/README.md`). Check it first.
  A folder with an approved `sheet.png` is a lock: never redesign that character.

This is a different world from the `khmer-cartoon-characters` skill (green-shirt boy, golden-outfit girl).
Don't mix the two casts in one film unless the user asks.

Priority: CHARACTER CONSISTENCY > STORY CONTINUITY > ANIMATION QUALITY > ENVIRONMENT DETAIL.

## 1. Core style (match the sheet — Style A; for Style B read its sheet: brighter colors, pure white background, rounder 3-head chibi proportions)
Clean 2D cartoon illustration at professional model-sheet quality:
- smooth clean dark-brown outlines, medium line weight, slightly thicker on the silhouette
- large expressive dark-brown eyes with one or two white highlights, visible upper lash line
- small rounded nose, simple expressive mouth, light rosy cheeks
- warm facial expressions, slightly exaggerated acting
- appealing family-friendly proportions (kids ~4 heads tall, adults ~6–6.5, king ~7)
- soft 2-tone cel shading with subtle highlights; no heavy gradients or texture
- clean readable silhouettes and costumes; detailed but animation-friendly
- warm palette: cream, deep red / maroon, dark brown, gold accents, warm skin tones
- warm light-neutral background (#efeae4-ish) for sheets

Never change the universe into photorealism, photography, 3D Pixar-style CGI, hyper-real renders,
Japanese anime, or western superhero comics.

## 2. Khmer visual identity
Use Cambodian influence where it fits, respectfully:
sampot-style skirts and wraps, krama scarves, gold ornamental belts and diamond buckles, traditional
jewelry (drop earrings, bangles, arm cuffs), Cambodian sandals, royal clothing and crowns inspired by
Angkor-era art, rural farm clothing, monk-inspired robes (only when the story calls for it, and shown
with respect), warrior clothing inspired by historical Khmer reliefs.

Don't mix in random Thai, Chinese, Japanese, European or fantasy costume elements unless the story
explicitly needs them.

## 3. Workflow for a new character
1. **Gather input** (ask only for what the user hasn't given; choose sensible defaults for the rest and say so):
   NAME · ROLE (hero / friend / teacher / mother / father / king / queen / warrior / farmer / villain /
   merchant / student / monk / child / animal / other) · AGE · GENDER (optional) · PERSONALITY ·
   STORY ROLE · COSTUME · MAIN COLORS · PROPS · SPECIAL FEATURES.
2. **Start from the closest template** in `references/templates.md` (young hero, girl friend, elderly
   mentor, young warrior, princess, king, villain, animal companion). Change it enough that the new
   character is clearly a different person: face shape, hairstyle, height and costume colors.
3. **Write the character bible** with the generator format in `references/templates.md` §New character:
   name, role, age, personality, background, visual design (face, hair, body, clothing, colors,
   accessories, props), 8–12 expressions, 6–10 poses, and the **identity lock** list.
4. **Write the image prompt** using the sheet prompt template + negative prompt in `references/templates.md`.
   Fill every bracket; paste the lock details into the prompt word for word.
5. **Save and show.** Create `characters/<name-lowercase>/` in the project root. Write the profile to
   `<name>.md` from `characters/_template/character.md` with Status: draft. Put the prompt and negative
   prompt in `prompt.txt`. Show both to the user. Generated attempts go in `drafts/`.
6. If the user generates an image and shares it, **run the quality check (§6)** against it and report
   each item as pass/fail. If an item fails, fix the prompt and regenerate it before approval.
7. **On approval,** copy the chosen image to `characters/<name>/sheet.png`, set Status: approved (date),
   and tick the quality checklist. The character is now locked. Check what is already there before overwriting.

For every important character the model sheet covers:
- **A. Front full-body.** Neutral stance, head to feet. Don't crop hair, hands, feet or accessories.
- **B. Three-quarter view (~45°).** Same face, hair, clothes, proportions, colors and accessories.
- **C. Side profile.** For animation reference.
- **D. Back view.** Clothing construction and hairstyle from behind.
- **E. Expressions (at least 8).** Happy, sad, angry, surprised, scared, confused, determined, laughing
  (optional: tired, crying, excited, thinking). The emotion changes; the identity never does.
- **F. Action poses (at least 6).** Walking, running, sitting, pointing, waving, thinking. Adventure
  characters add jumping, climbing, fighting stance, carrying an object, and looking back while running.

## 4. Identity lock (after approval)
Lock and never change: face shape, eye shape, iris color, skin tone, hairstyle, hair color, nose, mouth,
height, body proportions, clothing design, accessory placement (say which side), shoe design, color
palette (hex codes).

- **Allowed to change:** expression, pose, camera angle, lighting, temporary dirt, rain, sweat, tears, movement.
- **Not allowed without an explicit instruction:** a different hairstyle, face or skin tone, a random
  costume, a changed age or body proportions, missing accessories, random jewelry, random shoes.

Record sides from the **character's** point of view and add "(viewer's left/right in front view)".
The master sheet's own action-pose area drifts (for example, the girl's hair changes from bun to long
loose hair). The front lineup is the authority, and drift like that is exactly what the lock prevents.

## 5. Cast lineups
When there are several characters, put them all full-body in one horizontal lineup on one ground line,
using the height ladder in `references/cast-bible.md`. A child hero is the shortest human, teens are
slightly taller, adults are normal height, the king and warriors are taller and stronger, and the elderly
mentor is adult height with a slight stoop. Animals are scaled naturally next to the humans. Scale must
never drift between references.

## 6. Final quality check (report each line)
✓ same face in every pose · ✓ same hairstyle · ✓ same eye color · ✓ same skin tone · ✓ same costume ·
✓ same footwear · ✓ same accessories (on the same side) · ✓ five fingers per hand (four fingers + thumb
visible when relevant) · ✓ clean silhouette · ✓ full body visible, no cropped feet ·
✓ expressions clearly readable · ✓ fits the master-sheet universe · ✓ ready for video animation.
If any item fails, correct the design or prompt before final approval.

## 7. Animation-ready rules
Designs must work for image-to-video, 2D animation, lip-sync, rigging, YouTube, TikTok, Reels and
Khmer cartoon series:
- clothing keeps the limbs readable (no sleeves or capes hiding the elbows or knees in the key poses)
- avoid tiny repeated ornaments that flicker. Gold detail should be a few bold shapes, not filigree.
- keep a flat color area on the face for mouth shapes. Beards must leave the mouth readable.
- give every character one strong color signature (Dara = red scarf + sash, Rotha = dark red cape, ...)

## 8. Using the characters in a film
To animate these characters in an MP4, use the `create-animation-2d` skill. All Style A cast rigs are
locked in `create-animation-2d/engine/cast_dara.py` (ids: dara, malis, sokha, veasna, bopha, jayavuth,
rotha, sophea, puppy, monkey, elephant). In a film's `story_chars.py`: `import cast_dara; cast_dara.register()`.
A new approved character gets a spec added there, reusing its hex colors, and a check sheet
(`engine/sheet.py <id>`) before any scene is rendered. Voice lines use VoxCPM2 (see AGENTS.md). A Khmer speaker must check
the Khmer audio before it is published.

## 9. Content rules
- Family-friendly. Villains are clever and intimidating, never grotesque or gory.
- Weapons are stylized and adventure-appropriate: no blood, and never pointed at the viewer in kids' content.
- Female royals and leaders are active, intelligent characters, not only people who need rescuing.
- Monks and sacred imagery are shown with respect and are never played for jokes.
