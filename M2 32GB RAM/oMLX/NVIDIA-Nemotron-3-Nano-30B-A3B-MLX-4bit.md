oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: NVIDIA-Nemotron-3-Nano-30B-A3B-MLX-4bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          2069.9       10.43   494.7 tok/s    96.6 tok/s       3.394   339.4 tok/s    18.18 GB
pp4096/tg128          6460.8       12.57   634.0 tok/s    80.2 tok/s       8.057   524.3 tok/s    18.25 GB

Continuous Batching — Same Prompt
pp1024 / tg128 · partial prefix cache hit
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          96.6 tok/s     1.00x   494.7 tok/s   494.7 tok/s      2069.9       3.394
2x         128.1 tok/s     1.33x   602.9 tok/s   301.4 tok/s      3396.9       5.395
4x         150.7 tok/s     1.56x   608.7 tok/s   152.2 tok/s      6729.0      10.127

Continuous Batching — Different Prompts
pp1024 / tg128 · no cache reuse
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          96.6 tok/s     1.00x   494.7 tok/s   494.7 tok/s      2069.9       3.394
2x         128.3 tok/s     1.33x   596.6 tok/s   298.3 tok/s      3432.6       5.428
4x         148.7 tok/s     1.54x   570.3 tok/s   142.6 tok/s      7181.9      10.625