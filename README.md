# Claude Sonnet 5 API (claude-sonnet-5 / claudesonnet5) — llm guide with published pricing

> **input $1.6; cached_input $0.16; cache_write_5m $2** — flat per-unit billing through the OpenAI-compatible APIMart gateway, $1 minimum top-up.

**[Live pricing](https://go.apimart.ai/k-d8ab70)** · **[Get an API key](https://go.apimart.ai/k-9f1e97)**

Everything here refers to **claude-sonnet-5** — also written **claudesonnet5** or **claude sonnet 5**.

## Pricing (observed, snapshot 2026-09-24)

| Tier | Price |
| --- | --- |
| `input` | $1.6 |
| `cached_input` | $0.16 |
| `cache_write_5m` | $2 |

## Cost at scale

| Volume | Cost |
| --- | --- |
| 100 | $160 |
| 1,000 | $1,600 |

## How to call it

```bash
curl --request POST --url https://api.apimart.ai/v1/images/generations \
  --header "Authorization: Bearer $APIMART_API_KEY" --header 'Content-Type: application/json' \
  --data '{"model":"claude-sonnet-5","prompt":"a modern cliffside villa at dusk","size":"16:9","n":1}'
```

Submit, keep the `task_id`, poll `GET /v1/tasks/{id}` until `completed`; the response carries the URL and the exact amount charged.

## Disclosure

Documents access through APIMart, a third-party API gateway; not affiliated with the model vendor.
