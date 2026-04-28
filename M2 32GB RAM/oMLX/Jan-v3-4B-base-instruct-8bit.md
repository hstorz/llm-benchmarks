oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: Jan-v3-4B-base-instruct-8bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          1545.9       15.45   662.4 tok/s    65.2 tok/s       3.509   328.3 tok/s     4.72 GB
pp4096/tg128          6278.1       19.54   652.4 tok/s    51.6 tok/s       8.759   482.2 tok/s     5.28 GB

Continuous Batching — Same Prompt
pp1024 / tg128 · partial prefix cache hit
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          65.2 tok/s     1.00x   662.4 tok/s   662.4 tok/s      1545.9       3.509
2x         111.0 tok/s     1.70x   655.8 tok/s   327.9 tok/s      3123.0       5.429
4x         146.2 tok/s     2.24x  2294.0 tok/s   573.5 tok/s      1785.3       5.288

Continuous Batching — Different Prompts
pp1024 / tg128 · no cache reuse
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          65.2 tok/s     1.00x   662.4 tok/s   662.4 tok/s      1545.9       3.509
2x         108.6 tok/s     1.67x   618.3 tok/s   309.1 tok/s      3312.4       5.671
4x         141.5 tok/s     2.17x  1104.1 tok/s   276.0 tok/s      2111.7       7.329