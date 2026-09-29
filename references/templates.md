# Templates — role starters, generator format, image prompt, negative prompt

Role templates are **starting points** for new characters. For the actual characters on the master sheet,
use `cast-bible.md`.

## Role templates

### Main young hero (e.g. Dara)
Age 12–14 · curious, kind, determined, sometimes unsure, refuses to give up.
Young Cambodian boy with warm medium skin, large expressive brown eyes, dark brown slightly messy hair,
a youthful rounded face, a friendly expression and slim adventurous proportions. He wears a cream
short-sleeved shirt, dark brown cropped pants, a deep-red Khmer waist sash, brown sandals and a small
shoulder bag.
The design tells his personality: soft eyes = kindness, messy hair = adventure, simple clothes = ordinary
background, red scarf/sash = strong identity.
- Expressions: friendly smile, excited, worried, disappointed, angry, focused, surprised, laughing,
  crying, determined.
- Actions: walking, running, studying, writing, climbing, falling, standing back up, planting a seed,
  looking toward the mountains, celebrating quietly.

### Girl friend / companion (e.g. Malis)
Age 12–14 · intelligent, energetic, positive, caring, brave.
Young Cambodian girl with large warm brown eyes, long dark hair (partly tied) and a small flower
decoration. She wears a cream traditional-inspired top, a deep-red Khmer skirt, a simple gold belt,
small earrings and sandals. No heavy royal jewelry: she should feel like a relatable kid.

### Elderly mentor (e.g. Lok Ta Sokha)
Age 65–75 · patient, wise, calm, sometimes humorous, supportive, never overpowered.
Long white hair, white eyebrows, a long white beard, kind eyes and a slightly curved posture. He wears a
cream robe, a golden-brown sash, simple sandals, and carries a wooden walking staff. He guides the
heroes instead of solving their problems.

### Young warrior (e.g. Veasna)
Age 18–22 · athletic young man (not oversized) with black tied hair and confident eyes. He wears a cream
upper garment, dark brown pants, a deep-red waist fabric, a gold ornamental belt, gold forearm guards
and a traditional-inspired short sword that stays family-friendly.

### Princess (e.g. Princess Bopha)
Age 18–24 · intelligent, diplomatic, kind, brave, responsible. Long black hair, warm brown eyes and
graceful features. She wears white and deep-red royal-inspired clothing, a gold crown, gold jewelry and an
ornamental belt. She is never just waiting to be rescued.

### King (e.g. King Jayavuth)
Age 40–50 · tall and powerful, with strong shoulders, dark hair, a beard and moustache, and a serious but
compassionate face. He wears a royal warrior outfit with deep-red fabric, gold chest ornaments, a gold
crown and a decorative belt. His posture is dignified.

### Villain (e.g. Rotha)
Age 35–45 · clever, manipulative, ambitious, calm, intimidating. Narrow expressive eyes, black tied hair,
a sharp beard, a lean athletic body and a dramatic silhouette. He wears dark charcoal clothing, a
dark-red cape and limited gold. He is never grotesque and stays appealing enough to fit the world.

### Animal companions
Use the same friendly 2D language: big expressive eyes and clear simple shapes. Examples: a
brown-and-white puppy (playful, loyal), a small brown monkey (curious, funny, expressive hands), a gray
baby elephant (big ears, friendly, playful). Once designed, an animal is locked like any character.

## New character generator — output format
```
CHARACTER NAME:
ROLE:
AGE:
PERSONALITY:
BACKGROUND:

VISUAL DESIGN
FACE:
HAIR:
BODY:            (height relative to Dara = 1.00, heads tall)
CLOTHING:
COLORS:          (name + hex for each: skin, hair, eyes, main garment, accent, footwear)
ACCESSORIES:     (with side: "his right hip (viewer's left)")
PROPS:

EXPRESSION SET:  8–12
POSE SET:        6–10

CHARACTER CONSISTENCY NOTES (IDENTITY LOCK):
- face shape / eye shape / iris color / skin tone
- hairstyle / hair color
- nose / mouth
- height / proportions
- clothing design / accessory placement / shoes
- palette hex codes
- signature color element

IMAGE GENERATION PROMPT:
(filled template below)
```

## Character sheet image prompt template
```
Create a professional 2D animation character sheet for:
[CHARACTER NAME]

Use the supplied Khmer 2D character reference sheet as the primary visual style reference.

Character: [DESCRIPTION — face, hair, body, height, with identity-lock details word for word]
Personality: [PERSONALITY]
Costume: [COSTUME]
Color palette: [COLORS]
Accessories: [ACCESSORIES with side]

Sheet layout:
Top row: front full-body, 3/4 full-body, side view, back view.
Middle row: 8 facial expressions: happy, sad, angry, surprised, worried, laughing, focused, determined.
Bottom row: 6 dynamic action poses: walking, running, sitting, waving, pointing, action pose.

Visual requirements:
clean white or light warm-neutral background, professional animation model sheet,
clean dark-brown line art, soft cel shading, warm Cambodian-inspired color palette,
large expressive eyes, clear silhouettes, consistent proportions,
consistent face across every pose, high-quality 2D animation concept art,
full body visible, no cropped feet, no text labels, no watermark.
```

## Cast lineup prompt
```
A professional 2D animation cast lineup in the style of the supplied Khmer 2D character reference sheet.
All characters full-body, standing side by side on one ground line, left to right: [LIST with heights
relative to the child hero]. Correct height differences: child shortest, teens slightly taller,
adults normal height, king and warriors tallest and strongest, elderly mentor adult height with a slight
stoop, animals scaled naturally. [Paste each character's lock line.]
Clean light warm-neutral background, clean dark-brown line art, soft cel shading, no text, no watermark.
```

## Scene / single-shot prompt
```
[CHARACTER NAME] ([lock line: face, hair, clothes, colors, accessories with side]) [ACTION / EXPRESSION]
in [SETTING], [CAMERA: wide / medium / close-up, angle], [LIGHTING / time of day].
2D cartoon illustration in the style of the supplied Khmer 2D character reference sheet,
clean dark-brown outlines, soft cel shading, warm palette, full body visible where framed.
```

## Negative prompt
```
photorealistic people, 3D CGI, Pixar-like 3D, anime redesign, western comic style,
different face between poses, random hairstyles, different skin tone between poses,
different costume colors, extra fingers, missing fingers, malformed hands, duplicate limbs,
cropped bodies, cropped feet, floating accessories, random weapons, random text, labels,
watermarks, logos, blurry faces, inconsistent character height, overly complex backgrounds,
Thai/Chinese/Japanese/European costume elements (unless requested)
```

## Style B additions
Put this at the start of the prompt, and attach `reference/style-b-bright-sheet.png` instead of the master sheet:
```
Style B. Use the supplied bright Khmer chibi character sheet (green-shirt boy, golden-outfit girl) as the
primary visual style reference — same face construction, big dark-brown eyes, rosy cheeks, head about 1/3
of total height, clean dark-brown outlines, soft cel shading, bright saturated colors, pure white background.
This is a NEW character: do not copy the green-shirt boy or the golden-outfit girl.
```
Add `green shirt with red sash, golden sampot outfit, pink flower bob hair` to the negative prompt
(so the new character doesn't turn into one of the two locked heroes).
