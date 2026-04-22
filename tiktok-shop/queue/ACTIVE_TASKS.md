# Active Tasks

## COMPLETED ✅

- `[done] Claude | TikTok Shop | Optimize the current live TikTok listings | 2026-04-21 | output: tiktok-shop/listings/optimized_listings.md — 9 listings ready to paste into Seller Center`
- `[done] Claude | Sourcing support | Replace blocked 5-item queue with 4 sourceable replacement products | 2026-04-21 | see NEXT_ADD_QUEUE.md`
- `[done] Claude | Repo sync | Unified repo, Codex redirected off old repos | 2026-04-21 | ed-empire-command is single source of truth`
- `[done] Both | Prompt sync | Shared prompt understanding written back to repo | 2026-04-21 | see tiktok-shop/SHARED_UNDERSTANDING.md`
- `[done] Claude + Codex | AI video pipeline | 5 MP4 videos rendered successfully at 22:24 2026-04-20 | see Projects/tiktok_shop/videos/output/ — 5 confirmed successes`
- `[done] Both | video 2015 | Searched entire repo and workspace — NOT FOUND | 2026-04-21 | recorded here and in SHARED_UNDERSTANDING.md`
- `[done] Claude | TikTok content queue | Packaged a posting-ready creator-style queue for the live dress lane | 2026-04-21 | see tiktok-shop/reports/POSTING_QUEUE_READY.md`
- `[done] Codex | Video tooling research | Logged stronger realism / try-on / image-to-video options and synced the still-first production choice | 2026-04-21 | see tiktok-shop/reports/VIDEO_PIPELINE_RESEARCH.md + GITHUB_VIDEO_TOOLING_RESEARCH.md`
- `[done] Codex | Realistic creator video | Generated Satin V-Neck Bodycon Dress still + MP4 through the unified Imagen -> Veo pipeline | 2026-04-21 | outputs: Projects/tiktok_shop/exports/v14_satin_vneck_bodycon_img.jpg + v14_satin_vneck_bodycon_final.mp4`
- `[done] Codex | Bikini refinement pass | Generated 3-piece cover-up bikini set variants and tightened motion/product-match constraints | 2026-04-21 | outputs: Projects/tiktok_shop/exports/v14_threepiece_coverup_bikini_final.mp4 + v14_threepiece_coverup_bikini_v3_final.mp4`
- `[done] Codex | Loungewear accuracy pass | Corrected the 3-piece lounge prompt from seller screenshot truth and generated a closer still with white contrast cami + rope drawstring | 2026-04-22 | output: Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_img.jpg`
- `[done] Codex | Loungewear motion retry | Checked new TikTok reference movement, removed the frozen-motion Veo prompt, and generated a fresh creator-motion MP4 from the corrected still | 2026-04-22 | outputs: Projects/tiktok_shop/exports/v14_3piece_crop_shorts_lounge_v3_veo.mp4 + v14_3piece_crop_shorts_lounge_v3_final.mp4`
- `[done] Codex | Catalog homey-curvy batch | Upgraded the generator to self-check outfit accuracy + curvy styling + homey backgrounds and rendered 6 fresh catalog MP4s under tag homey_curvy_0422 | 2026-04-22 | outputs: Projects/tiktok_shop/exports/v14_*_homey_curvy_0422_final.mp4`

## BLOCKED — waiting on Ed

- `[blocked] Ed-only | TikTok Seller Center | Log in → paste optimized copy from tiktok-shop/listings/optimized_listings.md → submit for review | blocker: manual login needed | ~15 mins`
- `[blocked] Codex | CJ browser add flow | Add 4 replacement products from NEXT_ADD_QUEUE.md | blocker: needs stable CJ + TikTok Seller Center session | 1-3 hrs`

## TODO (unblocked — can start now)

- `[todo] Both | AI video pipeline | Run veo_v14_dress_pipeline.py against the current live TikTok product set and keep using the Imagen -> Veo path instead of the slideshow fallback | none | see tiktok-shop/reports/VIDEO_PIPELINE_RESEARCH.md`
- `[todo] Codex | Loungewear refinement pass | Compare the fresh v3 motion clip against the seller media and tighten framing / garment fidelity if needed | none | target outputs: v14_3piece_crop_shorts_lounge_v3_final.mp4 + seller screenshot`
- `[todo] Codex | Exact garment match | Pull the original CJ / TikTok seller image pack for the bikini set so the next pass can target true 1:1 garment fidelity instead of prompt-only matching | blocked only by source image availability | strongest future path: garment-preserving try-on`
- `[todo] Codex | Bikini homey-curvy rerun | Re-run `v14_threepiece_coverup_bikini_v3_homey_curvy_0422` through Veo after quota resets so the fresh still becomes a matching MP4 | blocked by current Veo quota | source still already exists`
- `[todo] Both | Dashboard | Keep dashboard.html updated with real TikTok state after each major step | none | ed-empire-command/dashboard.html`

## Rules

- Browser-driving work is single-threaded
- Do not re-research products unless explicitly requested
- Optimize TikTok Shop listings before heavy AI video generation
- Current blocked queue truth: the 5 queued expansion products are NOT_FOUND on TikTok and unavailable in the live CJ Add Product modal
- `video 2015` truth: checked on 2026-04-21 and not found in the shared repo
- Posting queue truth: current live dress lane has a ready-to-run 5-video creator-style queue in `tiktok-shop/reports/POSTING_QUEUE_READY.md`
- Split work evenly to conserve credit usage and avoid duplicated work
- Keep the repo loop/check cadence active when the work is heavy and tied to business execution
- Current heavy-work cadence: check and act every 3 minutes
- The goal is to complete and improve revenue-producing agents and pipelines, not just monitor them
