# TikTok Shop Status
**Updated:** 2026-04-22

- Shopify: LIVE
- CJ connection: LIVE
- Optima Connector: LIVE
- Products verified in Shopify: 4 confirmed in the short status path
- TikTok Seller Center: RECOVERABLE BUT UNSTABLE
- TikTok Shop counts: Active 6 | Reviewing 2 | Needs attention 7
- TikTok Shop listing optimization: ✅ DONE — `tiktok-shop/listings/optimized_listings.md`
- Product videos: ✅ REAL PIPELINE WORKING — Imagen 4.0 → Veo 2.0 (NOT the slideshow fallback)
- Video pipeline script: `Projects/tiktok_shop/bots/veo_v14_dress_pipeline.py` (new unified script)
- Revenue: $0 (pre-launch)

## Honest blocker truth

- Seller Center has been recovered to `Products > Manage products`, but session and browser state are still unstable.
- CJ and TikTok automation still depend on live browser/session health, not missing code.
- The original 5-product expansion queue is blocked upstream because those items are not currently sourceable in the CJ add-product flow.

## Blocked queue (NOT FOUND in current CJ flow)

- Body Contour Maxi Dress
- Cloud Knit Two-Piece Skirt Set
- Ribbed Lounge Flare Set
- Sherpa Trim Denim Shacket
- Contour Sculpt Zip Jacket

## Replacement queue (sourceable direction)

- Linen Blend Midi Wrap Dress
- Floral Chiffon Tiered Maxi Dress
- Butter Soft Wide-Leg Lounge Set
- Satin Ruched Slip Midi Dress

## Listing Optimization

- **Status:** DONE (2026-04-21, Claude Code)
- **Output:** `tiktok-shop/listings/optimized_listings.md`
- Covers all 9 products: 5 currently in Seller Center + 4 replacement queue items
- Each listing has: keyword-rich title, hook description, full benefit-led copy, correct category path, recommended price
- Ready to paste directly into TikTok Seller Center — no rewriting needed

## AI Video Pipeline Truth (2026-04-21)

- **Real pipeline:** Google Imagen 4.0 → Veo 2.0 (confirmed working since Apr 20)
- **DO NOT USE:** `run_product_videos.py` → this runs the FFmpeg slideshow fallback (catalog image + text = NOT what Ed wants)
- **USE THIS:** `python veo_v14_dress_pipeline.py` (covers 6 products, diverse models, mirror-selfie style)
- **Existing real MP4 outputs:** `Projects/tiktok_shop/exports/` — model_veo_latina_v1.mp4, kling_slim_veo_v2.mp4, pajama_set_tiktok_v3.mp4
- **Fresh output from this sync:** `Projects/tiktok_shop/exports/v14_satin_vneck_bodycon_final.mp4`
- **Fresh reference still from this sync:** `Projects/tiktok_shop/exports/v14_satin_vneck_bodycon_img.jpg`
- **Bikini set outputs from this sync:** `Projects/tiktok_shop/exports/v14_threepiece_coverup_bikini_final.mp4`, `v14_threepiece_coverup_bikini_v3_final.mp4`
- **3-piece loungewear exact-truth pass:** corrected from seller media to `white fuzzy contrast cami + matching cardigan/shorts + visible white rope drawstring`
- **Corrected loungewear still from screenshot truth:** `Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_img.jpg`
- **New reference video checked on 2026-04-22:** `https://www.tiktok.com/@thymetravelerswife/video/7626516407651421454`
- **Reference movement truth:** full-body room shot, phone-to-face creator framing, visible but restrained body movement, no slideshow energy, no frozen mannequin energy
- **GitHub research:** `tiktok-shop/reports/VIDEO_PIPELINE_RESEARCH.md`
- **GitHub tooling note:** `tiktok-shop/reports/GITHUB_VIDEO_TOOLING_RESEARCH.md`
- **`video 2015`:** NOT FOUND — checked entire repo and workspace (Apr 21)
- **Upgrade path when ready:** Kling 3.0 API (better fabric physics) — details in research notes
- **Exact-match blocker:** we still do not have the original CJ / TikTok seller image pack locally for the bikini set, so the current workflow can get close on look and vibe but can still drift on exact garment cut
- **Motion prompt fix on 2026-04-22:** replaced the old "living photograph / frozen" Veo prompt with a restrained creator-motion prompt
- **Fresh corrected loungewear MP4:** `Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_final.mp4`
- **Fresh corrected loungewear raw Veo clip:** `Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_veo.mp4`

## What is left

1. ~~Keep optimizing the current live TikTok listings first~~ ✅ DONE — copy is in `tiktok-shop/listings/optimized_listings.md`
2. **Ed:** Log into TikTok Seller Center → paste optimized content from listings file → submit for review
3. **Codex:** Add 4 replacement products via CJ browser flow → Shopify → Optima → TikTok
4. Verify CJ -> Shopify -> Optima -> TikTok end-to-end for each replacement product
5. Run and post the current live-product AI video queue while replacement products move through sync

## Ed-only actions

1. Manually re-login when TikTok Seller Center drops again
2. Keep the correct live commerce browser tabs available

## Coordination

- Codex task file: `agents/tiktok-shop.md`
- Both Claude + Codex write updates HERE (not to TikTok Shop Business 1 folder)
