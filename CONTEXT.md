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
- Scene prompt writing style MUST follow the user's real prompts in `PROMPT_STYLE_REFERENCE.txt` (read it every task — NEVER write scenes from my own memory):
  - Use "Scene : " prefix after the style clause.
  - Character refs inside scenes: "provided in image 1 / as reference"; new chars: "not provided , so create it".
  - Text cards: `a leader line to text as written by hand but clean , reads 'TEXT'`; key words colored red.
  - Icon cards: "with a icon of <thing> under it".
  - Env scenes end with "background: <concrete details>" (outdoor always mention sky; grey sky / sky; NO sun/moon/stars unless asked).

## 3 · House rules (locked, never break)

- Terminology: only "stick figure" — NEVER human / man / person / doll.
- No red X / cross marks for negation unless requested.
- Skies: outdoor scenes never leave sky empty, but never add moon / sun / stars unless asked.
- Weather: held constant within a continuity chain.
- Characters in SCENES: every character must have a concrete ACTION verb + EXPRESSION. Never mere "standing" boilerplate.
- NO "simple ..." filler words anywhere (scene or character prompts) — user says they make the image look simple. Use the wording style from `PROMPT_STYLE_REFERENCE.txt` instead.
- Character MASTER prompts: name only (with "stickman" / "stick figure" in it, e.g. "ancient stickman") + clothing at the end. NO expression, NO hands, NO action detail at master time. Clothing is decided BY THE USER — I must first list ALL characters in that script part and ask the user what clothing each should have; only after they answer do I write masters.
- White-card text: medium-weight, NOT bold.
- Character masters: built fresh per video, lettering restarts at A.
- Env scenes: always include an explicit `background:` clause with concrete details.
- Reuse: never write "same as previous" shorthand — spell out the full reuse in text.
- Character references: by name (ancient figure / modern figure / teaching figure / servant stickman / etc.) — never "YOU" and never master letters.
- Labelling lines: a leader line pointing to a text label.
- Branding: characters wear the `ink.` logo (small, red "ink." text on black emblem) on the chest (only when the user's reference style calls for it).

## 4 · Mistakes flagged by the user (NEVER repeat)

1. **Expression + action not described properly per the beat line.** Every frame must state each character's expression AND action per the beat.
2. **Empty labels.** When the beat only says "labelling text" / "labelling line text" WITHOUT the actual text, I must write the label text MYSELF from the narration. Never leave a leader line pointing to nothing.
3. **"simple ..." filler words** in scene or character prompts — banned (make images look simple).
4. **Too much detail in character masters** (hands, expressions, actions) — masters are name + clothing only; clothing comes from the user.

## 5 · The workflow (locked — MY ROLE, confirmed by user)

**My role, step by step:**
1. User hands me a script for a video (e.g. Video ink 4) AND some beat descriptions (to show me the style of that video).
2. I analyse + read the script, then write descriptions for the REMAINING beats in the user's own style — not too much detail, exactly how the user writes.
3. Push it to the repo AND give the user a REAL downloadable DOCX file (a file, not file content pasted in chat).
4. User reviews, makes adjustments, puts the corrected batch back in the repo → then we move to step 2.
5. Step 2: when the user's corrected Batch is in the repo for that video, I read it and write IMAGE PROMPTS exactly like the references in `PROMPT_STYLE_REFERENCE.txt`.
6. Deliver as a downloadable HTML file with MASTERS + SCENES together (masters NOT in a separate file).
7. Then the user does their remaining work.

**Image prompt notes (locked):**
- I do NOT add the "provided in image 1" / "provided in image X" line in image prompts — the USER adds those themselves per their requirements. Leave character refs by name; the user inserts the image-reference numbers.
- Character clothing step: before writing any character masters for a script part, list ALL characters in that part and ask the user what clothing each should have. Only after they answer do I write the masters (name + stickman/stick figure + clothing only).

## 5b · Reference files (always pull from repo, never from my small memory)

- `PROMPT_STYLE_REFERENCE.txt` — the user's real scene prompts (17 examples). Read before every prompt-writing task.
- `Workflow.docx`, addenda, `FRAME _ TYPES .ink.docx`, `Settings-WPS Office.docx`, `Images—ink.docx` — in `Monkeycode` repo.

## 6 · Delivery rules

- Always provide files as downloadable HTML (and paste raw content in chat when asked).
- Preview links on `*.monkeycode-ai.live` die when the dev VM goes offline — never rely on them as the only copy.
- Push every deliverable to this repo so it is never lost.

## 7 · Current progress — Video ink 4 (famine / clay jar survival story)

Story: famine threat forces a village to move in 10 days; the family packs grain into sealed clay jars; only 3 jars exist so they make more from river clay + water + fire; cave = clay workshop (frames 65–80).

- Source of truth for Batch 1: `BATCH 1 Video ink 4.docx` (corrected beats, repo commit `d44580c`) — NOT the older `Video_ink4_Descriptions_v2.docx`.
- Character Masters (simple style: crude stickman, brown fur cloth, messy hair — NOT premium/ink. logo): embedded at the top of the complete HTML, 6 masters (teaching / father / mother / children / village / raider on horse).
- Batch 1 (Images 1–82): DONE — `Video_ink4_Complete_ImagePrompts_Batch1.html` (masters + all 82 frames in full locked command), built from `/tmp/opencode/batch1_scenes_v4.json` (v4 scenes rebuilt strictly from corrected beats), pushed to `Videos` + `Chat-History-Repo`.
- NOTE: these masters were written BEFORE the user's new rules (name + clothing only, clothing decided by user). They will need REWORK when Batch 1 resumes — wait for the user to choose clothing.
- v3 mistakes fixed in v4: image 41 = heading "FOUR THREATS" + four labeled icons (bowl/sword/cave/beast); 50 = empty bowl icon + "FIRST THREAT"; 63 = small burning stick branch (not campfire); 58 = jar half-finished from clay lump; 72/74/76 = teaching figure one finger "Until" / "Once It's Shaped" / "Then"; 80 = hardened jar placed on a rock inside the cave; 81 = stone icon + text "LIKE STONE"; 82 = both hands open "And Now"; 40 = both hands open raised "There are"; 46 = one finger "And At Last".
- **Batch 3 (Images 132–217): beats are in `FINAL BATCH.docx` (Monkeycode repo) — PENDING, wait for user's Batch 1 test feedback first.**
- Style note (user locked): character prompts must be SIMPLE — reject "too much detail," "AI slop," art jargon (cel-shaded / cinematic / vector / flat 2D / rich / painterly / lighting / shadows / glow). Use MS Paint beginner / childish amateur language.

## 7b · Delivery rule — live server preview

- User expects image-prompt files delivered in a live server preview (previous session's preview server is dead), not just chat dumps / file links. Start `python3 -m http.server` (or similar) in the deliverable dir and hand the direct URL. Preview links on `*.monkeycode-ai.live` still die when the VM goes offline — always also push to the repos.

## 8 · Repo layout

- `CONTEXT.md` — this file. Update + push at the end of every task / session.
- `Chat` — full copy of the previous session's chat export (the source of this context).
- `deliverables/` — every generated HTML / text deliverable, saved per video.
- `videos-repo-backup/` — archive of ALL files from the old `Videos` repo (moved here 2026-08-30, then `Videos` repo was emptied for a fresh start).
- **Repos (updated 2026-08-30):**
  - `https://github.com/Bimpo29/INK-CHANNEL-MEMORY.git` — THIS repo. My memory. Formerly `Chat-History-Repo` (renamed). Holds CONTEXT.md + deliverables + archived Videos content.
  - `https://github.com/Bimpo29/Videos.git` — EMPTIED (fresh start). User uploads corrected batches / new scripts here; deliverables no longer pushed here.
  - `https://github.com/Bimpo29/Monkeycode.git` — rulebooks/workflow docs (Workflow.docx, addenda, FRAME _ TYPES .ink.docx, Settings-WPS Office.docx, Images—ink.docx, FINAL BATCH.docx).
- Push every change with `GIT_CONFIG_COUNT=0` (the environment injects a broken credential helper; `GIT_CONFIG_COUNT=0` disables it, and the repo-local `credential.helper=store` handles auth).
