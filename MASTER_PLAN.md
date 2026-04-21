# Ed's Empire — Master Monetization Plan
**Last Updated:** 2026-04-21  
**Owner:** Ed (Texas virtual wholesaler)  
**Agent Coordinator:** Claude Code + Codex

---

## How This Repo Works

- `/agents/` — each disciple reads + writes their task file here
- `/status/` — live status per project (agent updates after each run)
- This file = single source of truth for timeline + monetization %

Both Claude Code (`claude` in terminal) and Codex (`codex` in terminal) can read/write this repo.
Run them in two separate terminal tabs simultaneously — they are fully independent CLI tools.

---

## Empire Monetization Dashboard

| # | Project | Agent | Status | Revenue Model | Price | % to Live | Est. Time to First $ |
|---|---------|-------|--------|--------------|-------|-----------|----------------------|
| 1 | Prop Firm Rinse | John + Daniel | **LIVE** | Gumroad info product | $97 | **95%** | Already earning |
| 2 | TikTok Shop (women's fashion) | TikTok Shop | **LIVE** | CJ dropship margin | ~$15-40/order | **70%** | 1-2 weeks (need TikTok listing approval) |
| 3 | AI Wholesaler Vault | Peter | Product ready | Gumroad info product | TBD | **80%** | 1 week (need Ed to list on Gumroad account) |
| 4 | Wholesale Automation | Andrew | Bugs to fix | Done-for-you SaaS/tool | TBD | **60%** | 3-4 weeks |
| 5 | Lead List Scraper | Matthew | Built | $497 all-in-one tool | $497 | **65%** | 3-4 weeks |
| 6 | Claude Automation Service | Luke | Built | $997 done-for-you | $997 | **60%** | 4-6 weeks |
| 7 | Trading Bot | Thomas | Paper trade phase | Internal tool / future SaaS | TBD | **50%** | 6-8 weeks |
| 8 | Content Engine | Philip | Bots built | Backend for all lanes | N/A | **55%** | Supports other lanes |
| 9 | AI Video TikTok Shark | Simon | Concept stage | TikTok monetization | N/A | **20%** | 8-12 weeks |
| 10 | TikTok Shop Clothes (Zara) | Zara | Setup pending | CJ dropship + TikTok native | ~$10-30/order | **15%** | 8-12 weeks |

---

## Step-by-Step Plan Per Project

### 1. Prop Firm Rinse — John + Daniel ✅ LIVE ($97/sale)
**Current blockers:**
- X/Instagram auth stale (run `manual_login.py --platform twitter` + `--platform instagram`)
- Blotato returning 401 (needs manual re-auth in browser)
- Facebook page blocked (app-only issue)

**Next 7 days:**
1. [ ] Fix X session → post 4x/day from tweet_queue.json (44 queued)
2. [ ] Fix Instagram session → post 1 Reel/day
3. [ ] Sign up for Apex Trader Funding affiliate ($100/referral) at apextraderfunding.com/affiliate → update `affiliate_links.py`
4. [ ] Post "Day 1 of 5" series → triggers TikTok DM bot
5. [ ] Push TikTok to 100 followers → unlock link-in-bio

**Revenue path:**
- TikTok organic → Gumroad link → $97 sale
- Apex affiliate in video descriptions → $100/referral
- Estimated: $97-$500/week within 30 days with consistent posting

---

### 2. TikTok Shop (Women's Fashion) — TikTok Shop Agent 🟡 LIVE (needs push)
**Current state:** 4 products verified in Shopify; CJ connected

**Next 7 days:**
1. [ ] Complete TikTok Shop merchandising setup (collections + theme)
2. [ ] Generate AI product videos via Kling for top 4 products
3. [ ] Submit products to TikTok Shop catalog review
4. [ ] Post 3 product demo videos/day on TikTok

**Revenue path:**
- TikTok in-app checkout → CJ ships → ~$15-40 margin/order
- Estimated: $0-$300/week once TikTok catalog approved (~2 weeks)

---

### 3. AI Wholesaler Vault — Peter 🟡 PRODUCT READY
**Current state:** FINAL.zip ready; needs listing on Ed's OTHER Gumroad account

**Next 3 days:**
1. [ ] Ed logs into oroaramacella@gmail.com Gumroad manually
2. [ ] Upload FINAL.zip, set price, publish
3. [ ] Peter pushes product link to wholesale Facebook groups + Reddit

**Revenue path:** Info product sale, set price $47-$197
**Estimated:** $200-$500/week once listed and marketed

---

### 4. Wholesale Automation — Andrew 🟠 2 BUGS TO FIX
**Current state:** 5-stage pipeline built; 2 bugs + overdue follow-ups

**Next 14 days:**
1. [ ] Andrew identifies + fixes 2 pipeline bugs
2. [ ] Test full pipeline end-to-end
3. [ ] List as service/tool offering
4. [ ] Launch outreach to 50 wholesale buyers/week

**Revenue path:** SaaS or done-for-you service, $97-$497/mo
**Estimated:** $500-$2,000/month at 60 days

---

### 5. Lead List Scraper — Matthew 🟠 BUILT NOT SOLD
**Current state:** Scraper + skip trace + text in one tool; project folder exists

**Next 14 days:**
1. [ ] Test scraper end-to-end on real list
2. [ ] Package as downloadable tool or hosted service
3. [ ] List on Gumroad at $497
4. [ ] Promote in wholesale/real estate FB groups

**Revenue path:** One-time $497 tool or $97/mo subscription
**Estimated:** $500-$1,500/month at 60 days with consistent promotion

---

### 6. Claude Automation Service — Luke 🟠 BUILT NOT SOLD
**Current state:** $997 done-for-you service; needs clients

**Next 21 days:**
1. [ ] Luke creates service landing page / Gumroad listing
2. [ ] Define 3 clear service tiers
3. [ ] Outreach: 20 DMs/day to small business owners via X + LinkedIn
4. [ ] Close 1 beta client at $497-$997

**Revenue path:** High-ticket service $997+ per client
**Estimated:** $997-$3,000/month at 60 days with 1-3 clients

---

### 7. Trading Bot — Thomas 🔴 PAPER TRADE PHASE
**Current state:** engine_v6.py + ed_strategy.pine done; needs paper trading validation

**Next 30 days:**
1. [ ] Run paper trading for 30 days minimum
2. [ ] Track win rate, drawdown, expectancy
3. [ ] If >60% win rate → connect live account (small size)
4. [ ] Future: package as subscription signal service

**Revenue path:** Personal trading profits first; subscription service later ($97-$297/mo)
**Estimated:** No revenue for 60-90 days minimum (patience required)

---

### 8. Content Engine — Philip 🟠 BACKEND ONLY
**Current state:** Bots built; supports John, Simon, all social lanes
**This is infrastructure, not a product.** Philip's job = keep all content pipelines fed.

**Next 7 days:**
1. [ ] Connect Blotato accounts (manual login required)
2. [ ] Verify Philip's queues feed correctly into John + Simon lanes
3. [ ] No direct monetization — supports other projects

---

### 9. AI Video TikTok Shark — Simon 🔴 CONCEPT STAGE
**Current state:** Concept only; no working code or product

**Next 30 days:**
1. [ ] Define exact product: TikTok content service vs tool vs SaaS
2. [ ] Build v1 using existing video_generator.py as base
3. [ ] Post 10 test videos to TikTok to validate hooks
4. [ ] Decide: productize or fold into TikTok Shop lane

**Revenue path:** TikTok monetization or productized service
**Estimated:** 60-90 days before any revenue

---

### 10. TikTok Shop Clothes — Zara 🔴 SETUP PENDING
**Current state:** Concept + agent registered; no CJ products connected yet

**Next 30 days:**
1. [ ] Connect CJ Dropshipping women's fashion catalog
2. [ ] Generate Kling AI product videos for top 10 items
3. [ ] Submit to TikTok Shop native checkout
4. [ ] Post 3-5 videos/day once approved

**Revenue path:** TikTok native checkout → $10-30 margin/order
**Estimated:** $0-$200/month at 60 days (competitive space, needs volume)

---

## Priority Stack (Do These First)

```
WEEK 1 (Money fastest):
  1. Fix X + Instagram auth for John → post daily
  2. List AI Wholesaler Vault on Peter's Gumroad → instant sales
  3. Sign up Apex affiliate → add to every TikTok description

WEEK 2:
  4. TikTok Shop merchandising complete → first product orders
  5. Fix Andrew's 2 pipeline bugs → Wholesale Automation ready
  6. Test Matthew's Lead List Scraper end-to-end

MONTH 2:
  7. Luke lands first $997 service client
  8. Thomas completes 30-day paper trade
  9. Simon defines AI Video product
  10. Zara launches TikTok Shop Clothes
```

---

## Total Revenue Projection

| Timeframe | Conservative | Optimistic |
|-----------|-------------|------------|
| 30 days | $200-$800 | $1,500-$3,000 |
| 60 days | $1,000-$3,000 | $5,000-$10,000 |
| 90 days | $2,000-$6,000 | $10,000-$20,000 |

**Biggest lever:** John's TikTok + X daily posting → Gumroad ($97) + Apex affiliate ($100/ref)  
**Second lever:** Peter's Vault listed + marketed (zero more build time needed)  
**Third lever:** Luke's first service client ($997)

---

## Running Both Claude + Codex in Terminal

```bash
# Terminal Tab 1 — Claude Code
claude

# Terminal Tab 2 — Codex
codex

# They are independent. Both can read/write files in this repo.
# Convention: Claude plans + coordinates. Codex executes code.
```

---

*This file is the ground truth. Agents update /status/ after each run.*
