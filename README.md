# Awesome Flat-Rate LLM APIs [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated, sourced list of LLM API providers that bill a **fixed price per period** (flat-rate, subscription, request-quota or budget plans) instead of pure pay-per-token. Useful for coding agents (Claude Code, Cline, Roo Code, Kilo Code, Aider, OpenCode, Continue, Codex) where token bills are hard to predict.

**Disclosure:** this list is maintained by the APIClaw team, and [APIClaw](https://apiclaw.biz) is one of the entries. Every entry, ours included, gets the same columns and a link to the provider's own pricing page. Prices were checked on **2026-10-26** and change often, so recheck before you buy. Corrections and additions welcome via pull request (please include an official source link).

**Estimate your own cost:** [LLM API Cost Calculator for Coding Agents](https://ankita37105.github.io/llm-api-cost-notes/calculator.html) compares per-token list prices, OpenRouter, Claude Pro/Max and request-based plans for your requests/day, token counts and cache-hit rate.

## Contents

- [How these plans meter usage](#how-these-plans-meter-usage)
- [Multi-provider flat-rate APIs](#multi-provider-flat-rate-apis)
- [Open-model subscriptions](#open-model-subscriptions)
- [Vendor coding subscriptions](#vendor-coding-subscriptions)
- [Pay-per-token, for comparison](#pay-per-token-for-comparison)
- [Choosing](#choosing)
- [Contributing](#contributing)

## How these plans meter usage

"Flat-rate" never means infinite. Each plan below caps usage in one of these ways, and the cap matters more than the headline price:

| Metering type | What is limited | Example |
|---|---|---|
| **Request quota** | Number of requests per day (sometimes weighted by model) | APIClaw |
| **Fair-use ceiling** | API-equivalent dollar value per day | OpenLimits |
| **Compute budget** | Dollar budget per month, drawn down at per-token rates | Standard Compute |
| **Periodic credits** | Credits that refill weekly | Electron Hub, Synthetic |
| **Rolling windows** | Usage per 5-hour session plus weekly limits | Claude Pro/Max, OpenCode Go |

## Multi-provider flat-rate APIs

| Provider | Price | Metering | Models (per provider) | Payment | Source |
|---|---|---|---|---|---|
| [APIClaw](https://apiclaw.biz) *(ours)* | $19, $39, $59, $69, $89, $99, $129 / month | Request quota: 500 to 8,000 requests/day, heavier models weighted (e.g. Claude Sonnet 5.5 = 2, Claude Opus 5.5 and GPT-6 Sol = 3, DeepSeek V4 Pro = 1); tokens per request not capped; resets 00:00 UTC. Free trial: 50 requests. | Claude, GPT, Gemini, Mistral, Llama, Cohere, Grok, DeepSeek, Qwen, Kimi, GLM | Crypto (NOWPayments) | [plans](https://apiclaw.biz/public/plans), [weights](https://apiclaw.biz/public/model_hub), [llms.txt](https://apiclaw.biz/llms.txt) |
| [OpenLimits](https://openlimits.app) | €10 / 24 h, €45 / week, €120 / month (Max), €299 / month (Ultimate) | "Unmetered" with a fair-use ceiling of $2,000/day in API-equivalent usage on Day, Week and Max; no daily ceiling on Ultimate. No free tier. | Claude (Opus, Sonnet, Haiku), GPT-6 family, GLM, MiniMax, DeepSeek | Stripe | [pricing](https://openlimits.app/pricing), [FAQ](https://openlimits.app/faq) |
| [Standard Compute](https://standardcompute.com) | $19, $39, $89, $249 / month (individual); $499, $999, $2,499 / month (teams) | Compute budget: fixed monthly budget ($20, $41, $95, $269, $549, $1,119, $2,849) drawn at model per-token rates; requests stop at the budget, no overages. Larger first-month budget as a launch offer. | Frontier and open models via smart routing | See vendor | [pricing](https://standardcompute.com/pricing), [budgets and limits](https://docs.standardcompute.com/budgets-and-limits) |
| [Electron Hub](https://www.electronhub.ai) | $10, $19, $39, $69, $129, $249 / month | Periodic credits: $8 to $200 of weekly credits, refilled Sunday 21:00 UTC; up to 200 free-model requests/day; 10 to 100 requests/minute by tier. Annual billing 20% off. | 600+ models, 150+ premium (GPT, Claude, Gemini, Grok, DeepSeek) | Creem, lava.top, Ko-fi | [pricing](https://www.electronhub.ai/pricing), [subscriptions](https://docs.electronhub.ai/billing/subscriptions) |

## Open-model subscriptions

| Provider | Price | Metering | Models | Source |
|---|---|---|---|---|
| [Synthetic](https://synthetic.new) | Go $9, Standard $30, Big $90 / month | Periodic credits: weekly credit limit that regenerates 2% every 202 minutes; extra usage at API pricing. | Open-weight models (GLM, Kimi, DeepSeek, Qwen, gpt-oss and others) | [pricing](https://synthetic.new/pricing), [rate limits](https://synthetic.new/rate-limits) |
| [OpenCode Go](https://opencode.ai/go) | Go $10, Go Plus $40 / month | Rolling windows: estimated requests per 5 hours plus a monthly dollar limit per model; usable from OpenCode or other agents. | Curated coding models (Kimi, GLM, MiniMax, DeepSeek, Qwen, GPT 6 Luna, Claude Haiku 5.5, Gemini 4 Argon and more) | [Go](https://opencode.ai/go), [docs](https://opencode.ai/docs/go/) |

## Vendor coding subscriptions

These are single-vendor plans, mostly tied to the vendor's own apps and tools rather than a general API key.

| Plan | Price | Metering | Notes | Source |
|---|---|---|---|---|
| [Claude Pro / Max](https://claude.com/pricing) | Pro $20/month ($17 billed annually); Max 5x $100/month; Max 20x $200/month | Rolling windows: limits reset every 5 hours plus weekly limits; no published message count | Includes Claude Code. Max adds $100 or $200/month of Claude Platform API credits. Claude models only. | [pricing](https://claude.com/pricing), [Max plan](https://support.claude.com/en/articles/11049741-what-is-the-max-plan) |
| [GLM Coding Plan (Z.ai)](https://z.ai/subscribe) | From $18/month | Plan usage allowance (see vendor docs) | GLM models for Claude Code, Cline, Kilo Code, OpenCode and other tools | [overview](https://docs.z.ai/devpack/overview) |

## Pay-per-token, for comparison

Not flat-rate, listed so you can compare like with like.

| Provider | Pricing | Source |
|---|---|---|
| [OpenRouter](https://openrouter.ai) | Provider list price per token, plus a 5.5% fee on credit purchases (Standard) or 8% (Business); 25+ free models at 50 requests/day | [pricing](https://openrouter.ai/pricing) |
| [Requesty](https://www.requesty.ai) | Model cost + 5% | [pricing](https://www.requesty.ai/pricing) |
| [Anthropic API](https://claude.com/pricing) | Per token, e.g. Claude Sonnet 5.5 $2 input / $10 output per MTok | [pricing](https://claude.com/pricing) |
| [OpenAI API](https://platform.openai.com/docs/pricing) | Per token, e.g. GPT-6 Sol $2 input / $10 output per 1M tokens (≤272K context) | [pricing](https://platform.openai.com/docs/pricing) |

## Choosing

- **Light or bursty use:** pay-per-token usually wins. Run your numbers in the [calculator](https://ankita37105.github.io/llm-api-cost-notes/calculator.html) first.
- **Heavy daily agent use on Claude or GPT:** compare request quotas (APIClaw), fair-use ceilings (OpenLimits) and compute budgets (Standard Compute) against your real call volume and context sizes.
- **Open-weight models only:** Synthetic, OpenCode Go and the GLM Coding Plan are cheaper entry points.
- **You live in Claude Code and its limits fit you:** Claude Pro/Max is the simplest option.
- **Compliance, invoices, SLAs:** go direct to the model vendor or an enterprise gateway.

Related: [openai-compatible-api-gateways](https://github.com/ankita37105/openai-compatible-api-gateways) (gateway comparison), [apiclaw-examples](https://github.com/ankita37105/apiclaw-examples) (configs for Claude Code, Cursor, Cline and SDKs).

## Contributing

Pull requests welcome. Each entry needs: a link to the provider's official pricing page, the price, and how usage is metered. No affiliate links, no unsourced claims, and please disclose if you work for the provider you add.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work. See [LICENSE](LICENSE).
