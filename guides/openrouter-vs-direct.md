---
layout: default
---

# Guide: OpenRouter vs direct — when the middleman is worth it

> Status: **DRAFT v1 (mostly verified)** — OpenRouter mechanics from their official FAQ; DeepSeek pricing from official docs. Region-specific payment facts pending monthly tests.

## The three ways to buy Chinese models from abroad

| | Direct (provider platform) | OpenRouter | Aggregator (e.g., SiliconFlow) |
|---|---|---|---|
| Per-token price | **Provider list price** (cheapest) | Same list price, **no markup** ✅ | Spread over list (TBD, we measure) |
| Extra fees | None known | Fee on credit purchases (card/crypto) ✅ | None known |
| Payment friction | China-first checkout 🧪 | Any card, instant ✅ | International sign-up ✅ |
| Model breadth | One family | Hundreds of models | 200+ hosted open-weights |
| Fallbacks if one provider fails | None | Automatic rerouting ✅ | Within their catalog |
| Rate limits | Provider tiers (often deposit-based) | OpenRouter's tiers | Their tiers |

## The math that matters (verified inputs)

1. **OpenRouter adds no per-token markup** — their stated model is a fee at credit purchase ([FAQ](https://openrouter.ai/docs/faq)). So your effective cost vs direct = that fee percentage, nothing more.
2. **DeepSeek's own price already has a 2× swing**: off-peak output $0.60/M vs peak $1.20/M. Peak = UTC 01–04 & 06–10 Mon–Fri. A US-based team effectively never touches peak; a European team does every morning.
3. **BYOK note** (✅ from OpenRouter FAQ): you can plug your own provider key into OpenRouter — free allowance on paid plans, then 5% of list cost — if you want their tooling without their credit system.

## Decision rules we'd publish

- Evaluating many models → **OpenRouter**, the credit fee buys breadth and instant cards.
- One model, high volume, US time zone → **direct**, and schedule batches into off-peak for a built-in 50% discount.
- You need Anthropic-style endpoints for open-weight Chinese models → **aggregator** (SiliconFlow publishes an Anthropic-format endpoint — rare).
- A gateway resells at >1.5× the provider list with no service attached → walk away.

## What we'll add after monthly tests

- Real checkout screenshots and minimum top-ups for each direct platform
- Measured aggregator spreads vs first-party prices
- Failure/latency notes per path

---
*Last verified: 2026-11-06 · Sources: openrouter.ai/docs/faq, api-docs.deepseek.com, docs.siliconflow.com*
