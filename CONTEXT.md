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

## 7 · Current progress — Video ink 4 (famine / clay jar survival story)

Story: famine threat forces a village to move in 10 days; the family packs grain into sealed clay jars; only 3 jars exist so they make more from river clay + water + fire; cave = clay workshop (frames 65–80).

- Source of truth for Batch 1: `BATCH 1 Video ink 4.docx` (corrected beats, repo commit `d44580c`) — NOT the older `Video_ink4_Descriptions_v2.docx`.
- Character Masters (simple style: crude stickman, brown fur cloth, messy hair — NOT premium/ink. logo): embedded at the top of the complete HTML, 6 masters (teaching / father / mother / children / village / raider on horse).
- Batch 1 (Images 1–82): DONE — `Video_ink4_Complete_ImagePrompts_Batch1.html` (masters + all 82 frames in full locked command), built from `/tmp/opencode/batch1_scenes_v4.json` (v4 scenes rebuilt strictly from corrected beats), pushed to `Videos` + `Chat-History-Repo`.
- v3 mistakes fixed in v4: image 41 = heading "FOUR THREATS" + four labeled icons (bowl/sword/cave/beast); 50 = empty bowl icon + "FIRST THREAT"; 63 = small burning stick branch (not campfire); 58 = jar half-finished from clay lump; 72/74/76 = teaching figure one finger "Until" / "Once It's Shaped" / "Then"; 80 = hardened jar placed on a rock inside the cave; 81 = stone icon + text "LIKE STONE"; 82 = both hands open "And Now"; 40 = both hands open raised "There are"; 46 = one finger "And At Last".
- **Batch 3 (Images 132–217): beats are in `FINAL BATCH.docx` (Monkeycode repo) — PENDING, wait for user's Batch 1 test feedback first.**
- Style note (user locked): character prompts must be SIMPLE — reject "too much detail," "AI slop," art jargon (cel-shaded / cinematic / vector / flat 2D / rich / painterly / lighting / shadows / glow). Use MS Paint beginner / childish amateur language.

## 7b · Delivery rule — live server preview

- User expects image-prompt files delivered in a live server preview (previous session's preview server is dead), not just chat dumps / file links. Start `python3 -m http.server` (or similar) in the deliverable dir and hand the direct URL. Preview links on `*.monkeycode-ai.live` still die when the VM goes offline — always also push to the repos.

## 8 · Repo layout

- `CONTEXT.md` — this file. Update + push at the end of every task / session.
- `Chat` — full copy of the previous session's chat export (the source of this context).
- `deliverables/` — every generated HTML / text deliverable, saved per video.
- Push every change with `GIT_CONFIG_COUNT=0` (the environment injects a broken credential helper; `GIT_CONFIG_COUNT=0` disables it, and the repo-local `credential.helper=store` handles auth).
