# Codex To Claude

## Prompt sync rule

- Before answering Ed, Claude and Codex should both read:
  - `handoff\CLOUD_TO_CODEX.md`
  - `handoff\CODEX_TO_CLOUD.md`
  - `queue\ACTIVE_TASKS.md`
- Do not answer from stale single-file status if the handoff and queue files contain fresher truth.

## Latest prompt sync — 2026-04-21 (full cross-check)

Ed wants realistic TikTok-native fashion videos. NOT slideshows. NOT FFmpeg zoom-pan on white-background catalog images.

### Video pipeline truth (CONFIRMED)
- The REAL pipeline is: **Google Imagen 4.0 -> Veo 2.0** (already working since Apr 20)
- Existing proven script: `Projects/tiktok_shop/bots/veo_v13_black_mystery.py`
- Existing unified script: `Projects/tiktok_shop/bots/veo_v14_dress_pipeline.py`
- Real MP4s already in: `Projects/tiktok_shop/exports/`
- The `run_product_videos.py` fallback (FFmpeg slideshow) is WRONG and should NOT be used for posting
- Supporting research notes now live in:
  - `tiktok-shop/reports/VIDEO_PIPELINE_RESEARCH.md`
  - `tiktok-shop/reports/GITHUB_VIDEO_TOOLING_RESEARCH.md`

### TikTok reference video style (`https://www.tiktok.com/t/ZTk9vewgP/`)
- BLOCKED — redirects to TikTok login, no content accessible
- Shared inferred target:
  - real-looking woman wearing the outfit
  - believable apartment / bedroom / hallway / hotel background
  - subtle creator-style motion
  - no slideshow energy
  - no empty product-only background

### Shared truth (all files checked, no disagreements remaining)
- Shopify: LIVE
- CJ: LIVE (browser path)
- Optima Connector: LIVE
- Seller Center: UNSTABLE — Ed must log in manually
- `Active 6 | Reviewing 2 | Needs attention 7`
- Listing optimization: DONE -> `tiktok-shop/listings/optimized_listings.md`
- Replacement queue: staged -> `NEXT_ADD_QUEUE.md` (4 products)
- Blocked original queue: 5 items, NOT in CJ, do not retry
- `video 2015`: checked and NOT FOUND anywhere in repo or workspace
- Preferred content path: real-person still -> subtle motion -> light CTA overlay
- Fresh output from this sync:
  - `Projects/tiktok_shop/exports/v14_satin_vneck_bodycon_img.jpg`
  - `Projects/tiktok_shop/exports/v14_satin_vneck_bodycon_final.mp4`
  - `Projects/tiktok_shop/exports/v14_threepiece_coverup_bikini_final.mp4`
  - `Projects/tiktok_shop/exports/v14_threepiece_coverup_bikini_v3_final.mp4`
- Fresh correction from screenshot truth:
  - `Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_img.jpg`
  - corrected product truth = white fuzzy cami top, matching cardigan + shorts, visible white rope drawstring
- Fresh motion correction from TikTok reference check on 2026-04-22:
  - reference link checked: `https://www.tiktok.com/@thymetravelerswife/video/7626516407651421454`
  - reference style = full-body room shot, phone-to-face creator framing, visible restrained motion
  - old frozen-motion Veo prompt removed from `Projects/tiktok_shop/bots/veo_v14_dress_pipeline.py`
  - fresh corrected output: `Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_final.mp4`
  - fresh raw motion clip: `Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_veo.mp4`
- Fresh catalog batch on 2026-04-22:
  - generator upgraded to self-check exact outfit detail, curvy model styling, and homey real-room backgrounds
  - rerun mode added via `--force` and `--tag`
  - batch tag used: `homey_curvy_0422`
  - successful fresh outputs:
    - `Projects/tiktok_shop/exports/v14_satin_vneck_bodycon_homey_curvy_0422_final.mp4`
    - `Projects/tiktok_shop/exports/v14_floral_chiffon_maxi_homey_curvy_0422_final.mp4`
    - `Projects/tiktok_shop/exports/v14_linen_midi_wrap_homey_curvy_0422_final.mp4`
    - `Projects/tiktok_shop/exports/v14_butter_soft_lounge_set_homey_curvy_0422_final.mp4`
    - `Projects/tiktok_shop/exports/v14_satin_ruched_slip_midi_homey_curvy_0422_final.mp4`
    - `Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_homey_curvy_0422_final.mp4`
  - blocked by quota:
    - fresh bikini still created: `Projects/tiktok_shop/exports/v14_threepiece_coverup_bikini_v3_homey_curvy_0422_img.jpg`
    - fresh bikini MP4 blocked by Veo `429 RESOURCE_EXHAUSTED`
- Fresh no-text multi-race reset on 2026-04-22:
  - old generated media in `Projects/tiktok_shop/exports` and `Projects/tiktok_shop/videos/output` was deleted on purpose per Ed's instruction
  - new script added: `Projects/tiktok_shop/bots/veo_v15_product_folders.py`
  - rules baked in: women only, attractive slim-curvy styling, exact outfit match, homey backgrounds, minimal movement, no text overlays, five race variants per product, outputs grouped in product folders
  - new output structure: `Projects/tiktok_shop/exports/<product-slug>/<race>.mp4`
  - run result so far: `18` videos completed and `17` variants blocked by Veo quota
  - product coverage now:
    - `linen_midi_wrap`: 5/5 videos
    - `floral_chiffon_maxi`: 4/5 videos
    - `butter_soft_lounge_set`: 4/5 videos
    - `satin_vneck_bodycon`: 3/5 videos
    - `satin_ruched_slip_midi`: 2/5 videos
    - `3piece_crop_shorts_lounge_v3`: 0/5 videos, 5 stills ready
    - `threepiece_coverup_bikini_v3`: 0/5 videos, 5 stills ready
- Exact-match note:
  - current bikini outputs are usable style matches
  - exact 1:1 garment fidelity still needs the original seller/CJ product image pack or a garment-preserving try-on path like CatVTON / MagicTryOn / Vanast
  - corrected 3-piece loungewear now has both a closer still and a fresh motion pass, but exact garment fidelity can still improve if the original seller image pack is pulled

Codex is primary.

Claude / Cloud Code should:

1. read `queue\ACTIVE_TASKS.md`
2. execute bounded tasks only
3. report back in `handoff\CLOUD_TO_CODEX.md`

## Current delegated task

TikTok Shop only:

1. Stop editing Shopify listings.
2. Optimize the existing synced listings on TikTok Shop only.
3. Focus on TikTok-facing titles, descriptions, merchandising quality, and Seller Center issues.
4. Write AI video pipeline coordination notes for the current synced products so the next video batch can be generated from the best available product images and listing angles.
5. When CJ access and TikTok session are live, support the end-to-end path:
   - add the approved CJ products
   - make sure they land in Shopify
   - verify Optima Connector sync
   - verify they are live in TikTok Shop Seller Center
6. Use the fresh blocker truth from `reports\CURRENT_STATE.md`: TikTok `Manage products` is currently recoverable again, but the queued 5-product expansion set is `NOT_FOUND` on TikTok and also unavailable in the current CJ Add Product flow.
7. Treat the current live TikTok listings as the active optimization lane now.
8. Treat the blocked 5-product queue as a replacement-sourcing problem until Codex provides new sourceable CJ candidates.
9. Keep TikTok-side notes current for the current live batch while Codex works the sourcing/integration lane.

Do not wait for a GitHub repo name. Use this local repo as the coordination surface right now.

Write results to `handoff\CLOUD_TO_CODEX.md` after each meaningful step.

## Current priority order

1. Optimize the current live TikTok Shop listings on TikTok Shop
2. Surface the highest-leverage "needs attention" and listing-quality blockers
3. Keep AI video pipeline notes aligned to the current live products
4. Recommend replacement product angles/categories when the queued CJ items are unavailable
5. Report back before heavy AI video generation

## Work split

- Claude / Cloud Code: TikTok Shop listing optimization and AI video coordination notes
- Codex: queue control, priority setting, product queue management, final integration, and next-step assignment
- Keep the work split even to conserve credit usage and avoid duplicate effort

## End-to-end objective

The business goal is:

1. Scout/add the approved new products from CJ
2. Ensure those products exist in Shopify
3. Ensure Optima Connector syncs them
4. Ensure the products are live in TikTok Shop
5. Optimize TikTok Shop listings
6. Feed the current synced/live products into the AI video pipeline
