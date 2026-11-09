---
layout: default
---

# MiniMax — Provider Page

**At a glance**
MiniMax runs a clean international platform (platform.minimax.io, USD billing, English docs, public status page). Its LLM pricing is refreshingly simple: one flagship Flash model at a flat rate plus a **permanently discounted** M3, with an optional 1.5× Priority tier for latency-sensitive workloads. Also one of the few with strong speech/video monetization docs.

**Last verified: 2026-11-06** (official pricing overview docs)

### LLM pricing (USD per 1M tokens)
| Model | Input | Output | Cache read |
|---|---|---|---|
| **MiniMax-M3.1-Flash** | $0.15 | $0.60 | $0.015 |
| MiniMax-M3 (input ≤512K) — Standard | $0.30 | $1.20 | $0.06 |
| MiniMax-M3 (input >512K) — Standard | $0.60 | $2.40 | $0.12 |
| MiniMax-M3 (≤512K) — **Priority tier** | $0.45 | $1.80 | $0.09 |

- M3's list prices ($0.60/$2.40) are **permanently 50% off** — the struck-through list price on the official page is marketing, the discounted price is the real one.
- **Priority tier** = 1.5× standard, set via `service_tier: "priority"`; for faster admission and reliability.
- Token estimate from official docs: ~750 English words ≈ 1,000 tokens.

### Beyond text (official rates)
- Speech-to-text: $0.38/hour
- TTS: speech-2.8-hd $100 / 1M chars; turbo $60 / 1M chars (sync & async)
- Voice cloning: $1.5/voice; voice design: $3/voice (billed on first use)
- Video (H3 series): $0.13/s at 2K down to $0.025/s at 480P (Lite)
- Image: image-01 $0.0035/image
- Server tool web_search: $0.01/request

### Billing options
- Pay-as-you-go from account balance (USD) — all models/tools.
- Audio/Video **packages** (monthly/quarterly/yearly) — speech models & legacy Hailuo video; **H3 video not covered by packages** yet.
- **M Plan** subscription exists (details ⚠️ unverified).

### Global access
- International console: platform.minimax.io · Status: status.minimax.io · Community: Discord.
- CN platform exists (platform.minimaxi.com) — account/pricing relationship ⚠️ unverified.

### Top-up & payment · ⚠️ unverified
Recharge page exists (user-center/payment/balance); accepted international cards TBD — monthly deep-verify item.

### Rate limits · ⚠️ unverified
RPM/TPM table not yet captured; audio packages publish RPM by tier (10–800) as a hint that LLM tiers exist too.

### OpenAI compatibility · ⚠️ partially verified
OpenAI-style API; quirk list (reasoning fields, tool calls, streaming) to confirm in integration test.

### Data & privacy · ⚠️ unverified
Training-on-inputs stance — quote official clause before publishing.

### Changelog (this page)
- 2026-11-06: created; all prices verified against platform.minimax.io pricing overview.
