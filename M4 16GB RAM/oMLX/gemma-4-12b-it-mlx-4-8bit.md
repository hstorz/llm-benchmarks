oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: gemma-4-12b-it-mlx-4-8bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          7702.7      106.79   132.9 tok/s     9.4 tok/s       7.809   131.3 tok/s     8.15 GB
pp4096/tg128         33845.3       87.22   121.0 tok/s    11.6 tok/s      44.923    94.0 tok/s     8.43 GB

Continuous Batching
pp1024 / tg128
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x           9.4 tok/s     1.00x   132.9 tok/s   132.9 tok/s      7702.7       7.809
2x          22.3 tok/s     2.37x   117.9 tok/s    59.0 tok/s     12770.2      28.869
4x          39.8 tok/s     4.23x    89.7 tok/s    22.4 tok/s     25166.6      56.948
