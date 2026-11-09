---
layout: default
---

# Guide: How to pay for DeepSeek API from outside China

> Status: **DRAFT v1** — paths marked `✅ verified` are confirmed from official docs; paths marked `🧪 to test` are scheduled for our monthly deep-verify with a real foreign account. We will not publish untested payment instructions as fact.

## The problem

DeepSeek's API is among the cheapest frontier-model APIs anywhere (see [provider page](../deepseek/)), but the platform's payment story was built for Chinese users first. This guide maps every current path, with real trade-offs.

## Path 1 — Direct from DeepSeek 🧪 to test

Platform: platform.deepseek.com. Refund policy (from official ToS §6.3, ✅ verified): refunds of the unspent balance are possible but **processed as a single lump sum** after review, with fees deducted.

What we will test with a foreign account in the next deep-verify:
- [ ] Which international cards are accepted at checkout
- [ ] Whether foreign-issued cards trigger extra verification
- [ ] Minimum top-up and currency conversion

## Path 2 — OpenRouter (the middleman) ✅ verified mechanics

OpenRouter resells DeepSeek models at **provider-list price with no markup**; its revenue is a fee charged when you purchase credits (card & crypto accepted; fee rate shown at checkout — [official FAQ](https://openrouter.ai/docs/faq)).

- ✅ Pros: instant card payment, one account for hundreds of models, no China-side friction.
- ⚠️ Cons: you pay the credit-purchase fee on every top-up; model availability/routing is OpenRouter's call.
- Best for: evaluation and low-volume use where convenience beats ~5% class fees.

## Path 3 — Aggregator clouds (SiliconFlow etc.) 🧪 to test

[SiliconFlow](../siliconflow/) hosts DeepSeek open-weight models with international sign-up. Whether its spread vs DeepSeek first-party pricing is worth it — we'll publish measured numbers after the payment tests.

## Path 4 — Third-party gateways ⚠️ caution

Independent resellers exist. If you use one: prepaid small, verify the token metering yourself against a known workload, and prefer ones that publish per-token prices and terms (this is exactly why we track providers publicly).

## Price sanity check before you pay anyone ✅ verified

DeepSeek `deepseek-flash`, USD per 1M tokens: input $0.15 (off-peak) / $0.30 (peak); output $0.60 / $1.20; cache-hit input $0.003. Peak = UTC 01:00–04:00 & 06:00–10:00 Mon–Fri — **all US business hours are off-peak**; European mornings are partially peak. If a reseller charges you more than ~1.5× these numbers, you're paying for convenience, not scarcity — decide that consciously.

---
*Last verified: 2026-11-06 · Tested paths will be updated after the next monthly deep-verify.*
