oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: Qwen3.5-27B-Claude-4.6-Opus-Distilled-MLX-4bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          9220.7       48.40   111.1 tok/s    20.8 tok/s      15.368    75.0 tok/s    15.77 GB
pp4096/tg128         35958.5       52.02   113.9 tok/s    19.4 tok/s      42.565    99.2 tok/s    16.13 GB

Continuous Batching — Same Prompt
pp1024 / tg128 · partial prefix cache hit
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          20.8 tok/s     1.00x   111.1 tok/s   111.1 tok/s      9220.7      15.368
2x          28.1 tok/s     1.35x   111.2 tok/s    55.6 tok/s     18421.3      27.534
4x          30.1 tok/s     1.45x   111.0 tok/s    27.8 tok/s     36891.2      53.910

Continuous Batching — Different Prompts
pp1024 / tg128 · no cache reuse
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          20.8 tok/s     1.00x   111.1 tok/s   111.1 tok/s      9220.7      15.368
2x          27.5 tok/s     1.32x   110.2 tok/s    55.1 tok/s     18581.2      27.896
4x          29.2 tok/s     1.40x   109.8 tok/s    27.4 tok/s     37294.8      54.799