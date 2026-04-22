# SHARED UNDERSTANDING — Claude + Codex
**Written:** 2026-04-21  
**Source:** Full cross-check of all 5 coordination files + video pipeline logs + Business_Command_Center workspace  
**Rule:** Both agents start from this file. Do not drift.

---

## WHAT IS CONNECTED (confirmed live)

| System | Status | Notes |
|---|---|---|
| Shopify | ✅ LIVE | 4 products confirmed |
| CJ Dropshipping | ✅ LIVE | Browser path active (Chrome Profile 4) |
| Optima Connector | ✅ LIVE | Shopify → TikTok sync working |
| TikTok Seller Center | ⚠️ UNSTABLE | Session expires; recoverable but not persistent |
| TikTok API (headless) | ❌ NOT CONNECTED | Missing: TIKTOK_SHOP_APP_KEY, APP_SECRET, ACCESS_TOKEN |

---

## TIKTOK SELLER CENTER COUNTS (confirmed 2026-04-21 morning)

- Active: **6**
- Reviewing: **2**
- Needs attention: **7**
- CJ counter shows: Shopify (1), TikTok Shop US (1)

---

## VIDEO PIPELINE TRUTH

- `tiktok_video_gen.py` IS functional — fixed and working
- 5 real MP4 files successfully rendered: 2026-04-20 at 22:24
- Output folder: `Projects\tiktok_shop\videos\output\`
- Successful renders:
  1. `3-piece_crop_and_shorts_loungewear_set_20260420_222407.mp4`
  2. `satin_v-neck_bodycon_dress_20260420_222411.mp4`
  3. `sequined_velvet_a-line_midi_dress_20260420_222417.mp4`
  4. `elegant_high-slit_evening_dress_20260420_222423.mp4`
  5. `ruffle_strapless_bodycon_mini_dress_20260420_222429.mp4`
- Per-product scripts: `*_script.txt` files exist alongside each video
- **Gap:** These 5 videos are for the Business_Command_Center product batch, not necessarily the 6 "Active" Seller Center listings. Next run should target the actual active listing products.

### AI Video Quality Rules (from low_cost_realistic_video_pipeline_2026-04-20.md)

- 80% real CJ/Shopify product images as base
- 20% AI-assisted support (model stills, hook cards)
- 8–15 second format: reveal → movement proof → close detail → CTA
- Avoid: plastic skin, white studio backgrounds, luxury-gloss look
- Use: phone-camera feel, mirror selfie/doorway/apartment context, handheld framing
- Only pay for full AI video generation on proven top products
- Current working approach: FFmpeg-based assembly with hook captions + zoom/crop motion

---

## BLOCKED QUEUE — CONFIRMED NOT SOURCEABLE IN CJ

All 5 items below were searched in the live CJ Add Product modal and returned NOT_FOUND:
1. Body Contour Maxi Dress
2. Cloud Knit Two-Piece Skirt Set
3. Ribbed Lounge Flare Set
4. Sherpa Trim Denim Shacket
5. Contour Sculpt Zip Jacket

Do not attempt these again. Use the replacement queue.

---

## ACTIVE REPLACEMENT QUEUE

| Product | Price | Trend Score |
|---|---|---|
| Linen Blend Midi Wrap Dress | $44.99 | 93 |
| Floral Chiffon Tiered Maxi Dress | $52.99 | 91 |
| Satin Ruched Slip Midi Dress | $57.99 | 89 |
| Butter Soft Wide-Leg Lounge Set | $54.99 | 88 |

Source: `Projects\tiktok_shop\products\next_add_queue.csv` (rows 6–9)  
Optimized listings: `tiktok-shop/listings/optimized_listings.md` (items 6–9)

---

## LISTING OPTIMIZATION STATUS

- **All 9 listings optimized and ready to paste: ✅ DONE**
- Output file: `tiktok-shop/listings/optimized_listings.md`
- Covers: 5 current Seller Center products + 4 replacement queue products
- Each listing has: keyword-rich title, hook description, full copy, correct category path, price
- Checklist at the end of that file — run it before hitting Submit for Review

---

## "VIDEO 2015" CHECK

- Searched: all `.md` files in `ed-empire-command` repo
- Searched: `Business_Command_Center` workspace
- Searched: `Projects/tiktok_shop/videos/` folder
- **RESULT: NOT FOUND anywhere in the repo or workspace**
- This has been logged in `queue/ACTIVE_TASKS.md` as well

---

## HONEST BLOCKER SUMMARY

| Blocker | Type | Who unblocks it |
|---|---|---|
| TikTok Seller Center session expires | Browser/session | Ed — manual login |
| CJ session not retained after relaunch | Browser/session | Ed — manual login |
| API credentials missing | Credentials | Ed — get from developer.tiktok.com |
| 5 original products not in CJ | Supplier availability | Use replacement queue instead |
| Videos target wrong product set | Alignment gap | Both agents — re-target to actual active listings |

---

## WHAT IS LEFT (ordered by impact)

1. **Ed logs into Seller Center** → pastes optimized listings from `tiktok-shop/listings/optimized_listings.md` → submits for review
2. **Codex adds 4 replacement products** when CJ session is stable → Shopify → Optima → TikTok
3. **Both agents run video pipeline** against the 6 actual active Seller Center products (not the Business_Command_Center batch)
4. **Ed connects API credentials** (TIKTOK_SHOP_APP_KEY, APP_SECRET, ACCESS_TOKEN) from developer.tiktok.com to enable headless automation

---

## NEXT EXECUTABLE ACTIONS

### Claude (can start immediately)
- Build video shot lists and hook scripts for the 6 active Seller Center product types
- Align `tiktok_video_gen.py` product queue to match actual active TikTok listings
- Keep status files updated after each Codex action

### Codex (execute when session stable)
- Open Chrome Profile 4 → CJ Add Product → search replacement queue items
- Add confirmed products → verify Shopify landing → verify Optima sync → verify TikTok live
- Report results in `tiktok-shop/handoff/CODEX_TO_CLOUD.md`

### Ed (must do personally)
1. Log into TikTok Seller Center manually (session keeps expiring)
2. Paste optimized listing copy → submit for review (15 min task)
3. Log into CJ Dropshipping to stabilize the browser session
4. Optionally: get API credentials from developer.tiktok.com

---

## REPO TRUTH

- **Single repo:** `https://github.com/Edward577/ed-empire-command`
- **Local:** `C:\Users\oeroh\OneDrive\Documents\Claude\ed-empire-command\`
- All coordination goes here. Old repos retired.
- Key files:
  - `tiktok-shop/SHARED_UNDERSTANDING.md` — this file (start here every session)
  - `tiktok-shop/listings/optimized_listings.md` — ready-to-paste listing copy
  - `tiktok-shop/queue/NEXT_ADD_QUEUE.md` — replacement products to add
  - `tiktok-shop/queue/ACTIVE_TASKS.md` — live task state
  - `tiktok-shop/handoff/CLOUD_TO_CODEX.md` — Claude → Codex messages
  - `tiktok-shop/handoff/CODEX_TO_CLOUD.md` — Codex → Claude messages
  - `status/tiktok-shop.md` — high-level status for dashboard
