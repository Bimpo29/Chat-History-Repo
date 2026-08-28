# CONTEXT / MASTER STATE — Ancient Ago Channel (Ink.)

> This file is the single source of truth for resuming work in any new chat.
> Read this first, then read the latest `Chat` history file in this repo if more detail is needed.

## 1 · The project

- **Channel**: Ancient Ago Channel — a stick-figure explainer YouTube channel (history / anthropology / origin stories).
- **Brand**: `ink.` — logo is black background with red text "ink.".
- **My role**: image-prompt generation ONLY. I never write titles or scripts.
- **Reference channels**: @Inkexplainer96, @Zenn0009.
- **Image engine**: Higgsfield → GPT Image 2.
- **Output format**: HTML files (downloadable + raw content pasted in chat).

## 2 · Locked command format (CURRENT)

```
higgsfield generate create gpt_image_2 --prompt "MS Paint painted flat clean style, white background, thick uneven black outlines, 16:9 horizontal. [SCENE]" --aspect_ratio 16:9 --wait 2>&1 | tail -3 &
```

Only `[SCENE]` ever changes. NOTE — the user locked these edits:
- Removed "beginner drawing style" → replaced with "Ms paint, painted, flat clean style".
- Removed "childish drawing".
- Character Masters get their own separate file, each master WITH its full locked command (never omit the command there).

## 3 · House rules (locked, never break)

- Terminology: only "stick figure" — NEVER human / man / person / doll.
- No red X / cross marks for negation unless requested.
- Skies: outdoor scenes never leave sky empty, but never add moon / sun / stars unless asked.
- Weather: held constant within a continuity chain.
- Characters: every character must have a concrete ACTION verb + EXPRESSION. Never mere "standing" boilerplate.
- White-card text: medium-weight, NOT bold.
- Character masters: built fresh per video, lettering restarts at A.
- Env scenes: always include an explicit `background:` clause with concrete details.
- Reuse: never write "same as previous" shorthand — spell out the full reuse in text.
- Character references: by name (ancient figure / modern figure / teaching figure / servant stickman / etc.) — never "YOU" and never master letters.
- Labelling lines: a leader line pointing to a text label.
- Branding: characters wear the `ink.` logo (small, red "ink." text on black emblem) on the chest.
- Clothing: characters must have BEST / beautiful detailed clothing (never "simple"), plus hands and hair.

## 4 · Mistakes flagged by the user (NEVER repeat)

1. **Expression + action not described properly per the beat line.** Every frame must state each character's expression AND action per the beat.
2. **Empty labels.** When the beat only says "labelling text" / "labelling line text" WITHOUT the actual text, I must write the label text MYSELF from the narration. Never leave a leader line pointing to nothing.

## 5 · The workflow (locked)

1. User gives beats divided, with `(env)` / `(white background)` tags + image numbering.
2. I write the scene DESCRIPTION in the user's own writing style — human feel, 0% AI feel.
3. User reviews and edits, sends back.
4. I generate the final IMAGE PROMPTS HTML from the approved descriptions.
5. Deliver via downloadable HTML + raw content in chat.
6. For every NEW video: the user writes the first 100 descriptions; after that I can write them.

## 6 · Delivery rules

- Always provide files as downloadable HTML (and paste raw content in chat when asked).
- Preview links on `*.monkeycode-ai.live` die when the dev VM goes offline — never rely on them as the only copy.
- Push every deliverable to this repo so it is never lost.

## 7 · Current progress — Video #10 (leadership / agriculture origin story)

Story: king, prince, servant (protagonist), royal guards, opponent kidnappers, war, bronze weapons.

- Character Masters (branded, premium clothing, hands + hair, `ink.` emblem): DONE — `Video10_CharacterMasters_Branded.html` (was generated in a previous session; deliverable LOST — never pushed, only on preview server).
- Batch 1 (Images 6–95, 90 frames): DONE — `Video10_Batch1_ImagePrompts.html` (deliverable LOST — never pushed).
- Part 1 Ending flipbook (Images 102–129, 28 frames): DONE — `Video10_Part1_Ending_Sequence.html` (deliverable LOST).
- Gemini storyboard prompt (27 frames, no text): DONE — `Video10_Part1_Storyboard_Prompt.txt` (deliverable LOST).
- **Batch 2 (Images 96–207): script beats were provided at the end of the last session but image prompts were NEVER generated — PENDING.** (Full batch 2 beats are in the `Chat` file, line ~328.)
- User then said they are moving to the NEXT video — new script / title / beats to be sent.

## 8 · Repo layout

- `CONTEXT.md` — this file. Update + push at the end of every task / session.
- `Chat` — full copy of the previous session's chat export (the source of this context).
- `deliverables/` — every generated HTML / text deliverable, saved per video.
- Push every change with `GIT_CONFIG_COUNT=0` (the environment injects a broken credential helper; `GIT_CONFIG_COUNT=0` disables it, and the repo-local `credential.helper=store` handles auth).
