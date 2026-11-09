---
layout: default
---

# Kimi (Moonshot AI) — Provider Page

**At a glance**
Kimi's K3.1 Pro is a 3T-class open-weight flagship with a 1M-token context that benchmarks near the strongest proprietary models. The international platform (platform.kimi.ai) is OpenAI-SDK compatible and affordable to unlock ($1 minimum top-up), but access is **tiered by your cumulative top-up amount** — heavy limits require heavier deposits. Note the K2 → K3 migration deadline (Dec 2026).

**Last verified: 2026-11-06** (official docs: pricing page structure, K3.1 Pro quickstart, model list)

### Models & specs
| Model | Context | Notes |
|---|---|---|
| `kimi-k3.1-pro` | 1,048,576 | flagship; thinking **always on**; `reasoning_effort` low/high/max (default max) |
| `kimi-k3.1-pro-highspeed` | 1,048,576 | 2–3× speed variant |
| `kimi-k3` | 1,048,576 | batch supported |
| `kimi-k2.7-code` / `kimi-k2.6` | 262,144 | **K2 series closed to new users Oct 31, 2026; full retirement planned end of Dec 2026** — don't start new work on K2 |

### Pricing
- Structure (verified): flat pay-as-you-go, **no context-length tiering**; billable items are cache writes (TTL 5min / 1h tiers), input (cache-hit vs miss rates), output. Prices exclude taxes — tax is computed at checkout by your jurisdiction.
- **Per-token numbers: ⚠️ unverified** — official price tables are client-rendered; capture in monthly deep-verify from an authenticated session.
- Batch API: 60% of standard price for `kimi-k3.1-pro` and `kimi-k3` (verified).
- File APIs (upload/extract): temporarily free (verified).

### Access & limits (verified mechanics)
- **Minimum top-up $1** unlocks flagship models.
- **Cumulative top-up amount determines your account tier** → concurrency, RPM, TPM, TPD. Exact tier table: ⚠️ unverified (docs/pricing/limits).
- Practical meaning: evaluation is cheap, but production throughput requires committed deposits — budget accordingly.

### Caching (verified)
Context caching is **automatic** for eligible request prefixes; hits bill at cached-input price, writes bill once per write. Cache stored in blocks — a partial trailing block cannot be cached and bills as a miss. Default TTL 5m; pass `prompt_cache_options.ttl: "1h"` for workloads with >5-minute gaps.

### OpenAI compatibility (verified quirks — these bite)
- Base URL: `https://api.moonshot.ai/v1` with the standard OpenAI SDK.
- **`temperature` / `top_p` are fixed** (1.0 / 0.95) — omit them from requests.
- Multi-turn & tool calls: return the **complete assistant message** unchanged (don't strip `reasoning_content`).
- Vision: no public image URLs — base64 or `ms://<file-id>` only; `content` must be an array.
- `max_completion_tokens` defaults to 131,072 (max 1,048,576).
- Structured output: `json_schema` with `strict: true`; parse `content`, never `reasoning_content`.
- **Web search tool is officially "being updated, not recommended for production"** — don't build on it yet.

### Global access
International platform: platform.kimi.ai (English docs, USD pricing with local tax at checkout). CN platform (platform.moonshot.cn) relationship: ⚠️ unverified.

### Top-up & payment · ⚠️ unverified
$1 minimum confirmed; accepted international cards TBD — monthly deep-verify item.

### Data & privacy · ⚠️ unverified
Training-on-inputs stance — quote official clause before publishing.

### Changelog (this page)
- 2026-11-06: created; structure/mechanics verified from official quickstart & pricing docs; per-token prices flagged unverified.
