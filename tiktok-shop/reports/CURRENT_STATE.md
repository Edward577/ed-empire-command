# Current State

## Persistent coordination rule

- Codex <-> Cloud Code coordination through the local repo is the default operating path.
- Codex and Cloud Code should behave like one coordinated team and keep work moving without waiting on the user.
- Do not re-wait on missing GitHub placeholders when the local coordination repo is available.
- Use the shared handoff files first:
  - `handoff\CODEX_TO_CLOUD.md`
  - `handoff\CLOUD_TO_CODEX.md`
  - `queue\ACTIVE_TASKS.md`
- While heavy business work is live, the local repo loops should check and act every 3 minutes.
- Keep the work split even to conserve credits.
- Keep the repo/loop active only when the work is heavy, business-critical, or revenue-producing.
- The default goal of the agents is to make money by completing and improving the active business agents, systems, and pipelines.
- Claude handles TikTok Shop-side optimization and live-status checks.
- Codex handles queue control, CJ -> Shopify -> Optima flow, integration, and next-step assignment.

## Claude return rule

- Claude / Cloud Code should rejoin the same repo-driven coordination path when available again.
- On return, Claude should check the shared handoff first instead of waiting for the user.
- Codex should continue assigning bounded work through the repo and pick up the next step whenever Claude finishes.

## External login dependency

- When Ed logs into CJ Dropshipping, resume the full product path immediately:
  1. source/add approved CJ products
  2. ensure they land in Shopify
  3. verify Optima Connector sync
  4. verify products are live on TikTok Shop

## Current execution note

- Seller Center official TikTok account is confirmed linked to the shop (`janesstore2` / `EDDYS STORES`)

- CJ Dropshipping live browser tab confirmed at `https://www.cjdropshipping.com/mine/products/myproducts`
- Playwright persistent attach is still blocked by locked Chrome Profile 4
- Codex is using the already-open desktop browser path as the fallback for CJ work
- A CJ-side action from the live browser opened a TikTok Seller Center product edit page, confirming the current browser path can cross into TikTok-side product editing without relaunching Chrome
- Video pipeline is now functional for the current 5-product batch and real MP4 outputs exist under `C:\Users\oeroh\OneDrive\Documents\Claude\Projects\tiktok_shop\videos\output`

## Fresh blocker truth

- The currently recoverable Seller Center Chrome tab is landing on a session-expired redirect:
  - `https://seller-us.tiktok.com/account/register?redirect_url=https%3A%2F%2Fseller-us.tiktok.com%2Fproduct%2Flist&ttp_session_expire=1`
- Desktop recovery proved the Seller Center Chrome window is still open, but the active recoverable tab is not a clean live products page right now.
- `refresh_tiktok_session.py` and `refresh_sessions.bat` now exist for session refresh attempts, but Chrome's cookie DB lock still blocks fully automatic refresh while Chrome remains open.
- Current browser-side truth is: video generation works, repo coordination works, but CJ -> Shopify -> Optima -> TikTok live verification is still blocked by session/browser state rather than missing code.
- Morning 2026-04-21 check: the visible desktop drifted back to Codex/Claude windows again, and the direct automation scripts still land on a TikTok session-expired redirect for product verification.
- Morning 2026-04-21 check: direct Playwright runs for `add_more_products.py` and `cj_to_tiktok_lister.py` still fail on Chrome Profile 4 persistent launch/lock, so the queued products are not honestly confirmed added yet.
- Morning 2026-04-21 CDP relaunch check: after relaunching Chrome Profile 4 with remote debugging, CJ opened on its login page and TikTok opened on the session-expired account/register redirect.
- Morning 2026-04-21 CDP relaunch check: current fresh-launch truth is that neither CJ nor TikTok retained a usable logged-in session for the commerce automation path.
- Morning 2026-04-21 live CDP recovery check: TikTok Seller Center was recovered back to `Products > Manage products`, and the visible page body again showed:
  - `Active 6`
  - `Reviewing 2`
  - `Needs attention 7`
  - `5 listings to be optimized`
- Morning 2026-04-21 live search check: all 5 queued expansion products were searched on the real TikTok `Manage products` page and returned `NOT_FOUND`.
- Morning 2026-04-21 CJ live browser check: the live Added Products page was recovered successfully and showed the current imported products plus store counts:
  - `Shopify (1)`
  - `TikTok Shop US (1)`
- Morning 2026-04-21 CJ add-product check: the `Add Product` modal opened successfully, but the queued products were not available upstream in the current CJ source flow.
- Morning 2026-04-21 CJ search truth: exact and broader keyword variants returned no usable matches in the Add Product modal, including:
  - `Body Contour Maxi Dress`
  - `Cloud Knit Two-Piece Skirt Set`
  - `Ribbed Lounge Flare Set`
  - `Sherpa Trim Denim Shacket`
  - `Contour Sculpt Zip Jacket`
  - `Body Contour`
  - `Maxi Dress`
  - `Cloud Knit Set`
  - `Two Piece Skirt Set`
  - `Ribbed Lounge Set`
  - `Denim Shacket`
  - `Zip Jacket`
- Current strongest blocker truth: the next-add queue is blocked upstream by CJ source availability, not by repo coordination, not by the TikTok listing page, and not by the AI video pipeline.
- Current safest execution path: optimize the current live TikTok listings now, keep the AI video pipeline moving on the existing products, and replace the blocked CJ expansion queue with new sourceable CJ candidates.

## Live Seller Center truth

- Real refreshed Seller Center browser session was confirmed
- `Products > Manage products` was reached
- Visible counts:
  - `Active 6`
  - `Reviewing 2`
  - `Needs attention 7`

## Shopify app

- Connector in use: `Optima Connector`

## Current objective

1. verify Shopify connector state
2. continue listing/add flow from the refreshed queue
3. optimize listings
4. then move into AI video generation
5. recover a clean Seller Center session/browser state so the commerce-side verification path can complete again

## Refreshed add queue

The active seasonal add set now includes 4 more spring/casual-upscale products so the shop can move toward 8+ total products:

- `Linen Blend Midi Wrap Dress`
- `Floral Chiffon Tiered Maxi Dress`
- `Butter Soft Wide-Leg Lounge Set`
- `Satin Ruched Slip Midi Dress`

These are already staged in:

- `C:\Users\oeroh\OneDrive\Documents\Claude\Projects\tiktok_shop\products\next_add_queue.csv`

They fit the current shop direction better than the blocked exact-match CJ queue:

- spring-to-summer transition
- more casual but still elevated
- higher-perceived-value women's fashion
- better mix of dresses and easy luxury lounge/set options

## Execution split

- Codex is primary and owns priorities/quality
- Claude handles bounded delegated work and reports back

## Reference business workspace

- `C:\Users\oeroh\OneDrive\Documents\Claude\Business_Command_Center\01_active_revenue\tiktok_shop_empire1`
