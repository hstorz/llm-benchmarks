oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: supergemma4-26b-abliterated-multimodal-mlx-4bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          1921.6       32.17   532.9 tok/s    33.5 tok/s       2.340   443.6 tok/s    14.24 GB
pp4096/tg128          6820.7       23.85   600.5 tok/s    44.0 tok/s       7.298   564.1 tok/s    14.71 GB

Continuous Batching
pp1024 / tg128
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          33.5 tok/s     1.00x   532.9 tok/s   532.9 tok/s      1921.6       2.340
2x          65.7 tok/s     1.96x   551.7 tok/s   275.9 tok/s      3554.5       4.092
4x          83.3 tok/s     2.49x   539.6 tok/s   134.9 tok/s      7017.0       8.132