# LLM Benchmark Comparison - MacBook Pro M2 Max (32GB RAM)

## Hardware Configuration
- **Device**: MacBook Pro M2 Max
- **System RAM**: 32 GB
- **VRAM**: 21.33 GB
- **Source**: all per-model benchmark `.md` files in this folder
- **Primary comparison**: `pp1024/tg128` single-request results
- **Batch scaling**: `Continuous Batching - Same Prompt` at `pp1024/tg128`

---

## Coverage

This summary now includes all 9 benchmark reports in this folder, including the previously missing:

- `Qwen3.6-27B-4bit`
- `supergemma4-26b-abliterated-multimodal-mlx-4bit`

---

## Models Compared

| Model | Parameters | Format |
|-------|------------|--------|
| Jan-v3-4B-base-instruct-8bit | ~4B | 8-bit |
| GLM-4.7-Flash-MLX-4bit | ~4.7B | 4-bit |
| Qwen3.5-9B-MLX-4bit | ~9B | 4-bit |
| supergemma4-26b-abliterated-multimodal-mlx-4bit | ~26B | 4-bit |
| Qwen3.5-27B-Claude-4.6-Opus-Distilled-MLX-4bit | ~27B | 4-bit |
| Qwen3.6-27B-4bit | ~27B | 4-bit |
| Qwen3.6-27B-nvfp4 | ~27B | nvfp4 |
| Qwen3-Coder-30B-A3B-Instruct-MLX-4bit | ~30B | 4-bit |
| NVIDIA-Nemotron-3-Nano-30B-A3B-MLX-4bit | ~30B | 4-bit |

---

## Quick Takeaways

- **Fastest text generation**: `NVIDIA-Nemotron-3-Nano-30B-A3B-MLX-4bit` at **96.6 tok/s**.
- **Best first-token latency**: `Jan-v3-4B-base-instruct-8bit` at **1545.9 ms TTFT**.
- **Lowest peak memory overall**: `Jan-v3-4B-base-instruct-8bit` at **4.72 GB**.
- **Lowest peak memory in the 26-30B group**: `supergemma4-26b-abliterated-multimodal-mlx-4bit` at **14.24 GB**.
- **Best memory efficiency**: `Jan-v3-4B-base-instruct-8bit` at **13.8 tg tok/s per GB**.
- **Slow cluster**: `Qwen3.5-27B-Claude-4.6-Opus-Distilled-MLX-4bit`, `Qwen3.6-27B-4bit`, and `Qwen3.6-27B-nvfp4` all land around **20 tok/s** with **8.7-9.2 s TTFT**.

---

## Primary Comparison (`pp1024/tg128`)

| Rank | Model | tg tok/s | TTFT (ms) | TPOT (ms) | pp tok/s | Peak Mem | 4x Speedup | tg tok/s per GB |
|------|-------|----------|-----------|-----------|----------|----------|------------|-----------------|
| 1 | NVIDIA-Nemotron-3-Nano-30B-A3B-MLX-4bit | 96.6 | 2069.9 | 10.43 | 494.7 | 18.18 GB | 1.56x | 5.3 |
| 2 | Qwen3-Coder-30B-A3B-Instruct-MLX-4bit | 75.0 | 1746.7 | 13.43 | 586.3 | 16.59 GB | 1.64x | 4.5 |
| 3 | Jan-v3-4B-base-instruct-8bit | 65.2 | 1545.9 | 15.45 | 662.4 | 4.72 GB | 2.24x | 13.8 |
| 4 | Qwen3.5-9B-MLX-4bit | 61.2 | 2558.4 | 16.46 | 400.2 | 6.67 GB | 1.51x | 9.2 |
| 5 | GLM-4.7-Flash-MLX-4bit | 50.8 | 2148.2 | 19.83 | 476.7 | 16.42 GB | 2.02x | 3.1 |
| 6 | supergemma4-26b-abliterated-multimodal-mlx-4bit | 33.5 | 1921.6 | 32.17 | 532.9 | 14.24 GB | 2.49x | 2.4 |
| 7 | Qwen3.5-27B-Claude-4.6-Opus-Distilled-MLX-4bit | 20.8 | 9220.7 | 48.40 | 111.1 | 15.77 GB | 1.45x | 1.3 |
| 8 | Qwen3.6-27B-nvfp4 | 20.1 | 8658.1 | 50.02 | 118.3 | 16.64 GB | 1.34x | 1.2 |
| 9 | Qwen3.6-27B-4bit | 20.0 | 9248.1 | 50.52 | 110.7 | 15.85 GB | 1.51x | 1.3 |

---

## Latency Ranking

| Rank | Model | TTFT (ms) |
|------|-------|-----------|
| 1 | Jan-v3-4B-base-instruct-8bit | 1545.9 |
| 2 | Qwen3-Coder-30B-A3B-Instruct-MLX-4bit | 1746.7 |
| 3 | supergemma4-26b-abliterated-multimodal-mlx-4bit | 1921.6 |
| 4 | NVIDIA-Nemotron-3-Nano-30B-A3B-MLX-4bit | 2069.9 |
| 5 | GLM-4.7-Flash-MLX-4bit | 2148.2 |
| 6 | Qwen3.5-9B-MLX-4bit | 2558.4 |
| 7 | Qwen3.6-27B-nvfp4 | 8658.1 |
| 8 | Qwen3.5-27B-Claude-4.6-Opus-Distilled-MLX-4bit | 9220.7 |
| 9 | Qwen3.6-27B-4bit | 9248.1 |

---

## Memory Ranking

| Rank | Model | Peak Memory |
|------|-------|-------------|
| 1 | Jan-v3-4B-base-instruct-8bit | 4.72 GB |
| 2 | Qwen3.5-9B-MLX-4bit | 6.67 GB |
| 3 | supergemma4-26b-abliterated-multimodal-mlx-4bit | 14.24 GB |
| 4 | Qwen3.5-27B-Claude-4.6-Opus-Distilled-MLX-4bit | 15.77 GB |
| 5 | Qwen3.6-27B-4bit | 15.85 GB |
| 6 | GLM-4.7-Flash-MLX-4bit | 16.42 GB |
| 7 | Qwen3-Coder-30B-A3B-Instruct-MLX-4bit | 16.59 GB |
| 8 | Qwen3.6-27B-nvfp4 | 16.64 GB |
| 9 | NVIDIA-Nemotron-3-Nano-30B-A3B-MLX-4bit | 18.18 GB |

---

## Useful Comparison Charts

### Text Generation Speed (Higher = Better)

```text
NVIDIA-Nemotron-30B   | ######################## | 96.6 tok/s
Qwen3-Coder-30B       | ###################      | 75.0 tok/s
Jan-v3-4B             | ################         | 65.2 tok/s
Qwen3.5-9B            | ###############          | 61.2 tok/s
GLM-4.7-Flash         | #############            | 50.8 tok/s
supergemma4-26B       | ########                 | 33.5 tok/s
Qwen3.5-27B-Dist      | #####                    | 20.8 tok/s
Qwen3.6-27B-nvfp4     | #####                    | 20.1 tok/s
Qwen3.6-27B           | #####                    | 20.0 tok/s
```

### Peak Memory (Lower = Better)

```text
Jan-v3-4B             | ######                   | 4.72 GB
Qwen3.5-9B            | #########                | 6.67 GB
supergemma4-26B       | ###################      | 14.24 GB
Qwen3.5-27B-Dist      | #####################    | 15.77 GB
Qwen3.6-27B           | #####################    | 15.85 GB
GLM-4.7-Flash         | ######################   | 16.42 GB
Qwen3-Coder-30B       | ######################   | 16.59 GB
Qwen3.6-27B-nvfp4     | ######################   | 16.64 GB
NVIDIA-Nemotron-30B   | ######################## | 18.18 GB
```

### Batch Scaling to 4x (Higher = Better)

```text
supergemma4-26B       | ######################## | 2.49x
Jan-v3-4B             | ######################   | 2.24x
GLM-4.7-Flash         | ###################      | 2.02x
Qwen3-Coder-30B       | ################         | 1.64x
NVIDIA-Nemotron-30B   | ###############          | 1.56x
Qwen3.6-27B           | ###############          | 1.51x
Qwen3.5-9B            | ###############          | 1.51x
Qwen3.5-27B-Dist      | ##############           | 1.45x
Qwen3.6-27B-nvfp4     | #############            | 1.34x
```

### Throughput per GB (Higher = Better)

```text
Jan-v3-4B             | ######################## | 13.8
Qwen3.5-9B            | ################         | 9.2
NVIDIA-Nemotron-30B   | #########                | 5.3
Qwen3-Coder-30B       | ########                 | 4.5
GLM-4.7-Flash         | #####                    | 3.1
supergemma4-26B       | ####                     | 2.4
Qwen3.5-27B-Dist      | ##                       | 1.3
Qwen3.6-27B           | ##                       | 1.3
Qwen3.6-27B-nvfp4     | ##                       | 1.2
```

---

## Notes on Batch Scaling

- The batch-speedup chart uses `Continuous Batching - Same Prompt` for all models.
- That keeps the comparison consistent and avoids mixing cache-hit and no-cache runs.
- `Qwen3-Coder-30B-A3B-Instruct-MLX-4bit` does not include a 4x `Different Prompts` row in its source file, so using the `Same Prompt` table avoids an uneven comparison.

---

## Accuracy: Not Measured

These are **performance benchmarks only**. Accuracy, reasoning quality, coding quality, and multimodal quality were **not measured** here.

To evaluate quality, you would still need:

- task-specific prompt tests
- coding and reasoning evals such as HumanEval, MMLU, or GSM8K
- side-by-side scoring on your real workloads

---

## Summary Recommendations

### If You Want The Highest Raw Throughput
Use `NVIDIA-Nemotron-3-Nano-30B-A3B-MLX-4bit`.

### If You Want The Lowest Latency And Lowest Memory
Use `Jan-v3-4B-base-instruct-8bit`.

### If You Want A Smaller Model With Strong Efficiency
Use `Qwen3.5-9B-MLX-4bit`.

### If You Want A Large Model With Lower Memory Pressure
Use `supergemma4-26b-abliterated-multimodal-mlx-4bit`.

### If You Are Considering The 27B Qwen Variants For Performance
Expect all three to perform similarly on this machine: about **20 tok/s** generation with roughly **15.8-16.6 GB** peak memory.
