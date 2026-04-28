oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: Qwen3.5-9B-MLX-4bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          2558.4       16.46   400.2 tok/s    61.2 tok/s       4.649   247.8 tok/s     6.67 GB
pp4096/tg128         10160.6       16.96   403.1 tok/s    59.4 tok/s      12.314   343.0 tok/s     6.97 GB

Continuous Batching — Same Prompt
pp1024 / tg128 · partial prefix cache hit
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          61.2 tok/s     1.00x   400.2 tok/s   400.2 tok/s      2558.4       4.649
2x          85.0 tok/s     1.39x   400.7 tok/s   200.3 tok/s      5111.1       8.122
4x          92.4 tok/s     1.51x   399.0 tok/s    99.8 tok/s     10264.7      15.804

Continuous Batching — Different Prompts
pp1024 / tg128 · no cache reuse
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          61.2 tok/s     1.00x   400.2 tok/s   400.2 tok/s      2558.4       4.649
2x          86.5 tok/s     1.41x   400.2 tok/s   200.1 tok/s      5117.1       8.078
4x          91.6 tok/s     1.50x   399.0 tok/s    99.8 tok/s     10266.8      15.858