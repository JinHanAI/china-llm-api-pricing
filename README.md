# china-llm-api-pricing

**Live API pricing & status for Chinese LLMs — community-maintained, every number sourced.**

Chinese model APIs (Qwen, GLM, Kimi, DeepSeek, MiniMax…) are often 3-10x cheaper than US equivalents, but the prices are scattered across vendor docs in two languages. This repo puts them in one machine-readable JSON file, with a source link on every entry.

> **As of: 2026-08-23** · Prices change weekly — always verify against the vendor doc before committing spend.

## Text model prices (per 1M tokens, USD list price)

| Model | Vendor | Input | Cached input | Output | Context | Status |
|---|---|---|---|---|---|---|
| [glm-5.3](https://docs.z.ai/guides/overview/pricing) | Zhipu / Z.ai | $1.40 | $0.26 | $4.40 | 1M | GA (API since Aug 19) |
| [glm-5.2](https://docs.z.ai/guides/overview/pricing) | Zhipu / Z.ai | $1.40 | $0.26 | $4.40 | 1M | GA |
| [qwen3.8-max](https://www.alibabacloud.com/help/en/model-studio/models) | Alibaba | $2.00 | — | $6.00 | 256K+ | GA (Model Studio) |
| [qwen3.5-flash](https://www.llmabacus.com/en/chinese-llm-api-pricing) | Alibaba | **$0.029** | — | *tbc* | — | cheapest input observed |
| [deepseek-v4-flash](https://www.morphllm.com/llm-api) | DeepSeek | **$0.14** | — | **$0.28** | — | GA |
| [deepseek-v4-pro](https://apidog.com/blog/chinese-llm-price-war-2026/) | DeepSeek | *tbc* | — | **$0.87** | — | cheapest frontier output |
| [kimi-k3](https://platform.kimi.ai/) | Moonshot | $3.00 | $0.30 | $15.00 | 1M | GA |
| [kimi-k2.5](https://openrouter.ai/moonshotai/kimi-k2.5) | Moonshot | $0.45 | — | $2.25 | 262K | GA |
| [minimax-m3](https://www.morphllm.com/llm-api) | MiniMax | $0.60 | — | $2.40 | — | cheapest >80% SWE-bench |
| [mimo-v2.5-pro](https://apidog.com/blog/chinese-llm-price-war-2026/) | Xiaomi | *tbc* | — | $3.00 flat | 1M | flat rate at 1M ctx |

For scale: the cheapest US model (GPT-5.6 Luna) is $0.20/$1.20 — deepseek-v4-flash undercuts it on both axes.

## Video model prices (per second)

| Model | Vendor | 720p | 1080p/other | Source |
|---|---|---|---|---|
| happyhorse-1.1 | Alibaba | $0.0988/s | $0.1278/s (1080p) | [OpenRouter](https://openrouter.ai/alibaba/happyhorse-1.1) |
| seedance-2.5 | ByteDance | ~$0.23/s | ~$0.10/s (480p) | Volcano Ark (GA Aug 7) |

## Use the data

```bash
curl -s https://raw.githubusercontent.com/JinHanAI/china-llm-api-pricing/main/china-llm-api-pricing.json
```

Schema: [`schema-v1.json`](schema-v1.json) · Unknown fields are `null` + a `note` — we never guess numbers.

## Contributing

Price changes welcome via PR — **every price PR must link the official vendor doc or a dated aggregator snapshot**; unsourced price edits will not be merged. Relay/markup prices are out of scope (official list prices only). See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[Apache 2.0](LICENSE). The price data itself is factual data compiled from public vendor pricing pages.

---

Maintained by [ChinaModelAPI](https://chinamodelapi.com) — one OpenAI-compatible key for all Chinese models, pay with USDT.
