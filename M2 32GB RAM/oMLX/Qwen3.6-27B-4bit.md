oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: Qwen3.6-27B-4bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          9248.1       50.52   110.7 tok/s    20.0 tok/s      15.664    73.5 tok/s    15.85 GB
pp4096/tg128         35818.7       50.72   114.4 tok/s    19.9 tok/s      42.261   100.0 tok/s    17.27 GB

Continuous Batching
pp1024 / tg128
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          20.0 tok/s     1.00x   110.7 tok/s   110.7 tok/s      9248.1      15.664
2x          28.5 tok/s     1.43x   110.7 tok/s    55.4 tok/s     18343.0      27.489
4x          30.2 tok/s     1.51x   110.1 tok/s    27.5 tok/s     36481.1      54.136