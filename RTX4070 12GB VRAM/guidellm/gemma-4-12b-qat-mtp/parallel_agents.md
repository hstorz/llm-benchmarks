# parallel_agents

**guidellm**: 0.6.0  **profile**: concurrent  **model**: http://192.168.0.99:8080  **data**: ['kind=synthetic_text,prompt_tokens=128,output_tokens=128,turns=3']  **duration**: 30.0s  **rate**: [10.0]

| strategy                | duration | requests             | rps  | tok/s | TPOT (ms/tok) | prompt_tok | output_tok |
| ----------------------- | -------- | -------------------- | ---- | ----- | ------------- | ---------- | ---------- |
| concurrent (workers=10) | 30.0s    | 22/31 (err=0, inc=9) | 0.70 | 94.31 | 87.37         | 228        | 128        |

### Strategy: concurrent (workers=10)

**Requests/s**: mean=0.70, p50=0.71, p95=0.79, p99=1.13, min=0.00, max=1.13, std=0.15

**Prompt Tokens**: mean=228.09, p50=270.00, p95=407.00, p99=411.00, min=142.00, max=411.00, std=85.21

**Output Tokens**: mean=128.00, p50=128.00, p95=128.00, p99=128.00, min=128.00, max=128.00, std=0.00

**TPOT (ms/tok)**: mean=87.37, p50=106.96, p95=115.34, p99=115.64, min=11.16, max=115.64, std=34.14

**Output Tokens/s**: mean=94.31, p50=88.56, p95=100.90, p99=192.73, min=80.76, max=192.73, std=20.14

**Prompt Tokens/s**: mean=168.05, p50=180.79, p95=265.74, p99=536.79, min=89.60, max=536.79, std=76.85

**Tokens/s**: mean=262.36, p50=264.94, p95=349.32, p99=703.97, min=170.36, max=703.97, std=88.02

**Scheduler**: queued_avg=11.94s, request_avg=11.18s, resolve_avg=9.78s

---
