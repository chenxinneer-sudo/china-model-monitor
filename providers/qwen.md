---
layout: default
---

# Qwen (Alibaba Cloud Model Studio) — Provider Page

**At a glance**
Alibaba's Qwen family is served through Alibaba Cloud Model Studio with a genuinely international footprint (Singapore, HK, Frankfurt, Virginia, Tokyo regions). Watch-outs: the **same model has different prices per region**, tiered billing by total input length, and a web of stackable/non-stackable discounts (batch vs cache). Docs quality is high and updated frequently.

**Last verified: 2026-11-06** (official intl pricing page, "Last Updated: Nov 05, 2026")

### Models & specs (flagships)
| Model ID | Modes | Notes |
|---|---|---|
| `qwen3.8-max` | Non-thinking + Thinking | flagship, context caching supported |
| `qwen3.7-max` | Non-thinking + Thinking | snapshot variants pinned |
| `qwen3.8-flash` / `qwen3.7-flash` | both | tiered pricing by input length |
| `qwen3.5-plus` / `qwen-plus` | both | tiered pricing |

### Pricing (USD per 1M tokens, International/Singapore region)
| Model | Input | Output |
|---|---|---|
| qwen3.8-max | $2.00 | $6.00 |
| qwen3.7-max | $2.50 | $7.50 |
| qwen3.8-flash | $0.15 | $0.47 |
| qwen3.7-flash (≤32K in) | $0.030 | $0.130 |
| qwen3.7-flash (32–256K) | $0.100 | $0.400 |
| qwen3.7-flash (256K–1M) | $0.200 | $0.800 |
| qwen3.5-plus (≤128K) | $0.115 | $0.688 |

**Same model, cheaper elsewhere:** qwen3.8-max is **$1.65 / $4.951** in the China (Beijing) and Global (HK/Frankfurt/Virginia/Tokyo) regions vs $2/$6 in Singapore. Some Global regions run limited-time **night discounts (22:00–08:00 UTC+8, up to 60% off)** on plus-tier models.

### Discount mechanics (the confusing part — read before budgeting)
- **Tiered pricing:** the whole request is billed at the tier of its total input length (a 100K-input request pays the 32–128K tier rate for ALL tokens).
- **Batch inference:** 50% off input AND output; **cannot stack** with context-cache discounts.
- **Context cache:** explicit cache *creation* bills at 125% of input price; cache *hits* at 10%. Worth it for long stable system prompts.
- Output price for thinking mode includes chain-of-thought tokens — budget for CoT volume.

### Free tier
1M tokens free on selected flagships — **Singapore region only**, valid 90 days from activation. Other regions: no free quota on most models.

### Regions
Singapore ("International"), China (Beijing), Hong Kong, Frankfurt, Virginia, Tokyo. Global deployment scope vs US/JP scope affects which price table applies — check the region selector in the pricing page before comparing quotes.

### Top-up & payment · ⚠️ unverified
Minimum top-up, accepted international cards, refund policy — to be tested in monthly deep-verify.

### Rate limits · ⚠️ unverified
Published RPM/TPM table not captured yet; free-quota accounts are throttled harder (amount TBD).

### OpenAI compatibility · ⚠️ partially verified
OpenAI-compatible endpoint exists (compatible-mode); exact base URL and quirk list (tool calls, streaming, reasoning fields) to be confirmed by integration test.

### Data & privacy · ⚠️ unverified
Training-on-API-inputs stance and data residency per region — quote official clause before publishing this section.

### Changelog (this page)
- 2026-11-06: created; prices verified against official intl pricing page (updated Nov 05, 2026).
