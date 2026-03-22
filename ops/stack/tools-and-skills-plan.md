# Tools & Skills Plan for 5minsbliss Ops

## Goal
Enable end-to-end production for:
- Blog longform
- IG carousel visuals
- YouTube video + voiceover

## Tooling layers

### 1) Writing + planning
- OpenClaw + ShrimpOps templates (already in place)
- ClawTeam for multi-agent parallel drafting

### 2) Image generation (IG carousel covers + visual cards)
Recommended options:
- OpenAI Images API (via `openai-image-gen` skill)
- Midjourney (manual export workflow)
- Fallback: Canva template-driven production

### 3) Voiceover / TTS (YT narration)
Recommended:
- ElevenLabs (already available in current OpenClaw config)
- OpenAI TTS as backup

### 4) Video assembly
Recommended stack:
- CapCut (manual, fast)
- or FFmpeg + script pipeline (automated)
- Optional: Runway/Pika for motion shots

### 5) Publishing integration
- Ghost (website scheduling)
- Instagram (carousel upload)
- YouTube Studio (video + metadata)

## Required skills (OpenClaw)
- Existing: `openai-image-gen`, `github`, `summarize`
- To add next (custom local skills):
  1. `ghost-publisher` (draft/schedule/check posts)
  2. `ig-carousel-factory` (turn article into slide pack)
  3. `yt-repurpose-studio` (script -> shot list -> upload checklist)

## Security / governance
- External publishing actions = human approval gate
- API keys stored only in env/secretrefs
- Keep generated assets versioned in repo

## Phase rollout
1. Phase 1: text-only repurpose pipeline (done)
2. Phase 2: image generation integration
3. Phase 3: voice + video render integration
4. Phase 4: scheduled multi-channel publish
