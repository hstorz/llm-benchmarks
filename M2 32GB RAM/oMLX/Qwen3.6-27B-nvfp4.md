oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: Qwen3.6-27B-nvfp4
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          8658.1       50.02   118.3 tok/s    20.1 tok/s      15.011    76.7 tok/s    16.64 GB
pp4096/tg128         34519.5       53.27   118.7 tok/s    18.9 tok/s      41.284   102.3 tok/s    17.00 GB

Continuous Batching — Same Prompt
pp1024 / tg128 · partial prefix cache hit
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          20.1 tok/s     1.00x   118.3 tok/s   118.3 tok/s      8658.1      15.011
2x          24.5 tok/s     1.22x   118.0 tok/s    59.0 tok/s     17360.1      27.818
4x          27.0 tok/s     1.34x   118.2 tok/s    29.6 tok/s     34653.0      53.593

Continuous Batching — Different Prompts
pp1024 / tg128 · no cache reuse
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          20.1 tok/s     1.00x   118.3 tok/s   118.3 tok/s      8658.1      15.011
2x          24.4 tok/s     1.21x   118.2 tok/s    59.1 tok/s     17331.9      27.832
4x          27.0 tok/s     1.34x   118.1 tok/s    29.5 tok/s     34682.2      53.645