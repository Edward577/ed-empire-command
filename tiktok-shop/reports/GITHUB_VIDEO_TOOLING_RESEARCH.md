# GitHub Video Tooling Research
**Updated:** 2026-04-21

## Sync Truth

- Claude Code and Codex synced on the same repo files before this research pass.
- The TikTok short link `https://www.tiktok.com/t/ZTk9vewgP/` was not directly inspectable from this environment.
- Style target is therefore inferred from Ed's description:
  - real-looking woman
  - outfit on body
  - believable apartment / bedroom / hallway / hotel background
  - creator-native TikTok energy
  - no slideshow energy
  - no empty product-only background

## Best External Options Found

### 1. Photorealistic virtual try-on / garment transfer

- `Zheng-Chong/CatVTON`
  - Best use: photorealistic try-on stills from garment + model inputs
  - Why it matters: strongest path if we want the exact Shopify garment transferred onto a person instead of prompting a generic inspired look
  - Tradeoff: heavier setup than the current local path

- `nawodyaishan/ar-fashion-tryon`
  - Best use: full-stack try-on workflow with CatVTON-style direction
  - Why it matters: practical reference for combining extraction + try-on + app layer
  - Tradeoff: more system weight than we need for fast same-day output

- `shadow2496/VITON-HD`
  - Best use: research-grade virtual try-on baseline
  - Why it matters: useful if we later need more exact garment-fit transfer logic
  - Tradeoff: older / more research-oriented than the fastest production path

### 2. Image-to-video / motion upgrade options

- `zai-org/CogVideo`
  - Best use: open image-to-video path if we want a self-hosted video model track later
  - Why it matters: flexible longer-term option for creator-style motion
  - Tradeoff: much heavier than the current cloud-backed path already working locally

- `princepainter/ComfyUI-PainterI2VforKJ`
  - Best use: ComfyUI image-to-video workflows
  - Why it matters: useful if Ed wants a visual node workflow similar to plugin-driven creator tooling
  - Tradeoff: still depends on a stronger local GPU setup and workflow overhead

### 3. Short-form assembly / pacing

- `gyoridavid/short-video-maker`
  - Best use: short-form assembly, captions, packaging, voiceover structure
  - Why it matters: good reference for turning generated media into TikTok / Reels / Shorts packages
  - Tradeoff: not focused on fashion realism by itself

## Best Practical Path Right Now

For this machine and this workspace, the strongest practical path is:

1. Generate a realistic reference still first
2. Animate that still into a subtle creator-style clip
3. Add only light TikTok-native text treatment in FFmpeg
4. Keep the scene grounded in real-looking interiors and believable on-body outfit presentation

Current local stack already supports this:

- `google.genai` is installed
- `ffmpeg` is installed
- earlier local Imagen / Veo scripts already produced the best realism seen so far in this workspace

## Current Decision

Use the local still-first path now:

- still generation: Imagen via existing local `google.genai` workflow
- motion generation: Veo via existing local `google.genai` workflow
- final polish: FFmpeg subtitle / CTA pass only

Do **not** use the fallback slideshow generator as the main creative path.

## Upgrade Path Later

If we want even better realism after the current lane is stable:

1. add a CatVTON-based still-generation branch for exact garment transfer
2. add a ComfyUI image-to-video branch for node-based motion control
3. keep FFmpeg only for light TikTok finishing, not for fake motion creation

## Repo Implication

The repo truth should now treat the content lane as:

- preferred: real-person still -> subtle motion -> light CTA
- avoid: product-only slideshows, floating garments, sterile backgrounds, heavy text-first edits
