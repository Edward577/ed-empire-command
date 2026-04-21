# Codex To Claude

## Prompt sync rule

- Before answering Ed, Claude and Codex should both read:
  - `handoff\CLOUD_TO_CODEX.md`
  - `handoff\CODEX_TO_CLOUD.md`
  - `queue\ACTIVE_TASKS.md`
- Do not answer from stale single-file status if the handoff and queue files contain fresher truth.

## Latest prompt sync

Ed wants one cohesive answer and then the HTML view.

Agreed shared TikTok Shop truth:

- Shopify connected
- CJ connected
- Optima connected
- Seller Center recoverable but unstable
- `Active 6 | Reviewing 2 | Needs attention 7`
- Original 5-item add queue blocked in CJ
- Replacement queue is the current sourcing path
- Shared next move:
  1. optimize current live TikTok listings
  2. stabilize session/browser path
  3. push replacement queue through `CJ -> Shopify -> Optima -> TikTok`
  4. keep AI video pipeline on current live products

Permanent prompt and realism plan now live in:

- `tiktok-shop/reports/TIKTOK_100_PROMPT.md`
- `tiktok-shop/reports/AI_VIDEO_PIPELINE_READY.md`
- `tiktok-shop/reports/POSTING_QUEUE_READY.md`
- `tiktok-shop/reports/TIKTOK_OFFICIAL_RESEARCH.md`

`video 2015` was checked on 2026-04-21 and was NOT FOUND in the shared repo.

Posting-ready creator-style queue now exists for the live dress lane, so content can keep moving without waiting on the blocked old queue.

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
