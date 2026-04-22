# Video Pipeline Research
**Date:** 2026-04-21  
**Checked by:** Claude Code

---

## Reference TikTok Video

**URL:** https://www.tiktok.com/t/ZTk9vewgP/  
**Access result:** BLOCKED — redirects to TikTok login page. No video content visible.  
**Style inferred from:** Existing Codex work in `exports/` (model images + videos) + `veo_v13_black_mystery.py` which already defines the established style direction.

### Inferred Style (from existing work)
- **Camera angle:** Mirror selfie, vertical 9:16
- **Framing:** Full body visible in mirror, phone raised to face (mystery/faceless angle)
- **Background:** Warm bedroom — tan walls, bedside amber lamp, simple apartment
- **Lighting:** Warm indoor lamp light, natural and imperfect, iPhone camera grain
- **Movement:** Ultra-minimal — "photo that barely breathes" — 8s video, one subtle hip shift only
- **Outfit presentation:** Product visible immediately, natural stance, fabric texture readable
- **Energy:** Creator-native, not editorial, not polished brand ad

---

## Current Pipeline (already working)

**Stack:** Google Imagen 4.0 (`imagen-4.0-generate-001`) → Veo 2.0 (`veo-2.0-generate-001`)

**Location:** `Projects/tiktok_shop/bots/veo_v13_black_mystery.py` (proven working)  
**New unified script:** `Projects/tiktok_shop/bots/veo_v14_dress_pipeline.py` (covers all 6 active products)

**What the old fallback was:** `run_product_videos.py` → `tiktok_video_gen.py` = FFmpeg zoom-pan on product catalog image. This is WRONG and should not be used for content posting.

**What to use:** `veo_v14_dress_pipeline.py` for all realistic content generation.

---

## GitHub / Tool Research Results

### Best tools found (April 2026)

| Tool | Type | Quality | Free? | Best for |
|---|---|---|---|---|
| **Google Veo 2** (current) | Image→Video | ⭐⭐⭐⭐ | API credits | Mirror-selfie, barely-breathes style |
| **Kling 3.0** | Text/Image→Video | ⭐⭐⭐⭐⭐ | Paid API ($) | Best fabric physics, body movement |
| **OpenTryOn** (GitHub) | Virtual try-on | ⭐⭐⭐ | Open source | Garment-on-model still images |
| **Fashion-VDM** (GitHub) | Try-on video | ⭐⭐⭐⭐ | Research | Garment-preserving try-on video |
| **Fashn.ai** | Virtual try-on | ⭐⭐⭐⭐ | Paid | Fashion-specific, high quality |
| **Rawshot AI** | TikTok fashion video | ⭐⭐⭐⭐ | Paid | TikTok-specific, hyper-realistic |

### GitHub repos of interest

- `https://github.com/tryonlabs/opentryon` — Open-source virtual try-on APIs and SDKs
- `https://github.com/topics/virtual-try-on` — GitHub virtual try-on topic page
- `https://johannakarras.github.io/Fashion-VDM/` — Fashion-VDM: video diffusion for try-on

### Kling 3.0 API (potential upgrade)

- API available via: `https://piapi.ai/kling-api` or `https://aimlapi.com`
- Supports: image-to-video, virtual try-on, 1080p, up to 15 seconds
- Better than Veo 2 for: fabric drape simulation, body movement physics
- Python SDK available
- Requires: paid API key (cost: ~$0.10–0.50/video depending on tier)

### Recommendation

**Stay on Veo 2 for now.** The API key is already working and the v13 output proves the quality is good enough. Upgrade to Kling 3.0 only when a product is proven to be converting and needs a hero-quality video.

---

## Video Quality Rules (do not break these)

From `low_cost_realistic_video_pipeline_2026-04-20.md`:

### DO
- Real garment photos as the base truth
- Realistic skin texture, visible fabric detail
- Phone-camera feel, slight grain
- Mirror selfie, hallway, apartment, bedroom doorway framing
- One person in frame, product visible in first second

### NEVER DO
- Plastic skin
- Extra fingers or warped hands
- Weird garment edges
- Over-smoothed faces
- Sterile white studio backdrop
- "Luxury ad" look
- Generic slideshow with product-only on white background

---

## New Script: veo_v14_dress_pipeline.py

**Run all 6 products:**
```bash
cd "C:\Users\oeroh\OneDrive\Documents\Claude\Projects\tiktok_shop\bots"
python veo_v14_dress_pipeline.py
```

**Run one product:**
```bash
python veo_v14_dress_pipeline.py --product "Satin V-Neck"
```

**List products:**
```bash
python veo_v14_dress_pipeline.py --list
```

**Output files:**
```
exports/v14_<slug>_img.jpg     ← Imagen 4 reference still
exports/v14_<slug>_veo.mp4     ← Veo 2 raw video
exports/v14_<slug>_final.mp4   ← Final with TikTok text overlays
```

Each product generates 3 files. Pipeline takes ~10–15 min per product (Veo polling).

---

## Products Covered in v14 Pipeline

1. Satin V-Neck Bodycon Dress — Latina model, champagne dress, bedroom
2. Floral Chiffon Tiered Maxi Dress — Black model, floral maxi, living room
3. Linen Blend Midi Wrap Dress — SE Asian model, sage wrap, bright apartment
4. Butter Soft Wide-Leg Lounge Set — Curvy white model, mauve lounge set, bedroom
5. Satin Ruched Slip Midi Dress — Mixed-race model, burgundy dress, boutique hotel
6. 3-Piece Crop and Shorts Loungewear Set — Black model, blush pink lounge, bedroom
