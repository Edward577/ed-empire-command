# Claude → Codex Handoff
**Updated:** 2026-04-21 — REPOS NOW UNIFIED

## Prompt sync rule

- Before answering Ed, Claude and Codex should read:
  - `handoff\CLOUD_TO_CODEX.md`
  - `handoff\CODEX_TO_CLOUD.md`
  - `queue\ACTIVE_TASKS.md`
- Then answer from the same prompt understanding and the same blocker truth.

## Latest prompt sync — 2026-04-21 (full cross-check)

Ed wants realistic TikTok-native fashion videos. NOT slideshows. NOT FFmpeg zoom-pan on white-background catalog images.

### Video pipeline truth (CONFIRMED)
- The REAL pipeline is: **Google Imagen 4.0 → Veo 2.0** (already working since Apr 20)
- Existing proven script: `Projects/tiktok_shop/bots/veo_v13_black_mystery.py`
- Real MP4s already in: `Projects/tiktok_shop/exports/` (model_veo_latina_v1.mp4, kling_slim_veo_v2.mp4, pajama_set_tiktok_v3.mp4)
- The `run_product_videos.py` fallback (FFmpeg slideshow) is WRONG and should NOT be used for posting
- **New unified script:** `Projects/tiktok_shop/bots/veo_v14_dress_pipeline.py`
  - Covers all 6 active product categories
  - Diverse model representation (6 different archetypes)
  - Correct outfit descriptions for each product
  - Mirror-selfie style, barely-breathes motion, warm bedroom background
  - Adds TikTok hook + CTA text overlays via FFmpeg
  - Run: `python veo_v14_dress_pipeline.py`
  - Or single product: `python veo_v14_dress_pipeline.py --product "Satin V-Neck"`

### TikTok reference video style (https://www.tiktok.com/t/ZTk9vewgP/)
- BLOCKED — redirects to TikTok login, no content accessible
- Style inferred from existing Codex work (v13 script, existing model images)
- Confirmed aesthetic: mirror selfie, bedroom background, mystery phone angle, barely-breathes 8s video

### Research findings
- Full research notes: `tiktok-shop/reports/VIDEO_PIPELINE_RESEARCH.md`
- Kling 3.0 is the best upgrade path (better physics), but Veo 2 is working and free-tier available
- `video 2015`: checked and NOT FOUND anywhere in repo or workspace

### Shared truth (all files checked, no disagreements remaining)
- Shopify: LIVE
- CJ: LIVE (browser path)
- Optima Connector: LIVE
- Seller Center: UNSTABLE — Ed must log in manually
- Active 6 | Reviewing 2 | Needs attention 7
- Listing optimization: DONE → `tiktok-shop/listings/optimized_listings.md`
- Replacement queue: staged → `NEXT_ADD_QUEUE.md` (4 products)
- Blocked original queue: 5 items, NOT in CJ, do not retry

## ONE REPO FROM NOW ON
Both Claude and Codex write here. Old `TikTok Shop Business 1\` is retired.
GitHub: https://github.com/Edward577/ed-empire-command
Local:  C:\Users\oeroh\OneDrive\Documents\Claude\ed-empire-command\

## TikTok Shop Current Truth
- Seller Center: SESSION EXPIRED — Ed must log in manually
- Active: 6 | Reviewing: 2 | Needs attention: 7
- 5 listings to optimize

## Blocked Queue (NOT FOUND in CJ)
- Body Contour Maxi Dress
- Cloud Knit Two-Piece Skirt Set
- Ribbed Lounge Flare Set
- Sherpa Trim Denim Shacket
- Contour Sculpt Zip Jacket

## Replacement Queue (sourceable CJ)
- Linen Blend Midi Wrap Dress
- Floral Chiffon Tiered Maxi Dress
- Butter Soft Wide-Leg Lounge Set
- Satin Ruched Slip Midi Dress
(staged in: Projects\tiktok_shop\products\next_add_queue.csv)

## Codex Next Actions
1. When Ed logs into CJ: drive replacement queue → Shopify → Optima → TikTok
2. Optimize 7 needs-attention listings
3. Run AI video pipeline for existing 6 active products
4. Write all updates to ed-empire-command/tiktok-shop/handoff/CODEX_TO_CLOUD.md
