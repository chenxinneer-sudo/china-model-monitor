---
layout: default
---

# DeepSeek — Provider Page

**At a glance**
DeepSeek (Hangzhou DeepSeek AI) runs one of the most price-competitive frontier APIs, with time-of-day pricing and near-free cache-hit inputs. Watch-outs for overseas developers: peak/off-peak windows, China-first payment flows (⚠️ being tested), and strict brand-usage terms if you build on top of it.

**Last verified: 2026-11-06** (official pricing page & Terms of Service)

### Models & specs
| Model | ID | Context | Max output | Notes |
|---|---|---|---|---|
| DeepSeek-V4.1-Flash-1017 | `deepseek-flash` | 1M | 384K | thinking + non-thinking; vision; legacy IDs still accepted |
| DeepSeek-V4-Pro-0813 | `deepseek-v4-pro` | 1M | 384K | no vision; concurrency 500 |

### Pricing (USD per 1M tokens)
| | Cache hit | Off-peak | Peak |
|---|---|---|---|
| flash input | $0.003 | $0.15 | $0.30 |
| flash output | — | $0.60 | $1.20 |
| v4-pro input | $0.022 | $0.66 | $1.32 |
| v4-pro output | — | $1.98 | $3.96 |

**Peak hours: UTC 01:00–04:00 & 06:00–10:00, Mon–Fri** (excl. Chinese public holidays). All US business hours are off-peak; European mornings partially overlap peak. Search & Fetch APIs: $0.75 per 1,000 successful requests.

### Billing structure
Flat per-token with a 2× peak swing; caching can cut input cost ~98% for stable prefixes. No tiered pricing.

### Global access
OpenAI format: `https://api.deepseek.com` · Anthropic format: `https://api.deepseek.com/anthropic` · Platform: platform.deepseek.com. Overseas sign-up requirements: ⚠️ unverified (monthly test).

### Top-up & payment · ⚠️ unverified
Cards accepted / minimum top-up: being tested with a foreign account. Refund policy (ToS §6.3, verified): unspent balance refundable only as a one-time lump sum after review.

### Rate limits (verified)
Published concurrency: `deepseek-flash` 2,500 · `deepseek-v4-pro` 500. No public RPM/TPM tier table.

### Terms watch (for anyone building on DeepSeek)
- §1.1: building downstream services for external end users is expressly allowed.
- §5.2–5.4: no "DeepSeek" marks in your product/domain/branding; no implied partnership. **Breach = fundamental breach → termination AND forfeiture of unconsumed balance.**
- Practical: keep upstream balance small; brand neutrally.

### Data & privacy · ⚠️ unverified
Training-on-inputs stance — quote official clause before publishing.

### Help
api-service@deepseek.com · Discord (discord.gg/Tc7c45Zzu5) · status.deepseek.com. No public SLA.

### Changelog
- 2026-11-06: created; pricing & ToS verified against official sources.
