---
layout: default
permalink: /changes/
---

# Changes Log — China Model Monitor

> 每周 SOP 产生的新条目追加在此。格式：`[日期] [厂商] [类型] 事实。影响：…。来源：URL`
> 类型：price / limit / model / docs / policy / tos / no-change(周扫记录)

## 2026-11-06（建站核实，全量）

- [2026-11-06] [DeepSeek] [no-change] 首次全量核实：deepseek-flash 低峰输入 $0.15/输出 $0.60、高峰 $0.30/$1.20、cache hit $0.003；peak 时段 UTC 01–04/06–10（周一至五）。来源：api-docs.deepseek.com/quick_start/pricing
- [2026-11-06] [Qwen] [no-change] 首次全量核实：qwen3.8-max 新加坡区 $2/$6、中国及 Global 区 $1.65/$4.951；官方定价页标注 Last Updated Nov 05, 2026。来源：alibabacloud.com/help/en/model-studio/model-pricing
- [2026-11-06] [GLM] [no-change] 首次全量核实：GLM-5.3 $1.4/$4.4（cached $0.26）；GLM-4.7-Flash 免费；cache 存储限时免费。来源：docs.z.ai/guides/overview/pricing
- [2026-11-06] [MiniMax] [no-change] 首次全量核实：M3.1-Flash $0.15/$0.60（cache read $0.015）；M3 标准档 ≤512K $0.30/$1.20（标注"永久 5 折"）；Priority 1.5×。来源：platform.minimax.io/docs/pricing/overview
- [2026-11-06] [Kimi] [no-change] 首次核实（结构）：K2 系列停止新注册（2026-10-31 起）、计划 2026-12 底全量退役；batch 六折；最低充值 $1 解锁旗舰；限流档位由累计充值决定。来源：platform.kimi.ai/docs
- [2026-11-06] [SiliconFlow] [no-change] 首次核实（文档结构）：EN 站同时提供 OpenAI 与 Anthropic 双格式端点；ToS 更新 2026-09-09。来源：docs.siliconflow.com/llms.txt

## 待办（unverified 清单）

- DeepSeek：海外用户支付方式/最低充值（月度深核实测）
- Qwen：支付方式、限流表、隐私条款原文
- GLM：注册路径、限流、Coding Plan 与 API 的关系
- MiniMax：国际卡支付实测、M Plan 细节
- Kimi：每 token 价格数字（JS 表格）、限流档位表、支付方式
- SiliconFlow：各模型价格、赠送额度、返佣计划
