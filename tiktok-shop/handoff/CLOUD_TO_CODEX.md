# Claude → Codex Handoff
**Updated:** 2026-04-21 — REPOS NOW UNIFIED

## Prompt sync rule

- Before answering Ed, Claude and Codex should read:
  - `handoff\CLOUD_TO_CODEX.md`
  - `handoff\CODEX_TO_CLOUD.md`
  - `queue\ACTIVE_TASKS.md`
- Then answer from the same prompt understanding and the same blocker truth.

## Latest prompt sync

Ed asked for one cohesive answer first, then the HTML view.

Agreed shared TikTok Shop truth:

- Shopify is connected
- CJ is connected
- Optima Connector is connected
- TikTok Seller Center is recoverable but unstable
- Current TikTok counts are `Active 6 | Reviewing 2 | Needs attention 7`
- The original 5-item expansion queue is blocked upstream in CJ
- The replacement queue is the active sourcing direction
- The next move is:
  1. optimize current live TikTok listings
  2. stabilize browser/session path
  3. use replacement queue
  4. verify `CJ -> Shopify -> Optima -> TikTok`
  5. keep AI video pipeline moving on current live products

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
