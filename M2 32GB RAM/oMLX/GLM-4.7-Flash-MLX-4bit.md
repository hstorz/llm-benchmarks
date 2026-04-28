oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: GLM-4.7-Flash-MLX-4bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          2148.2       19.83   476.7 tok/s    50.8 tok/s       4.666   246.9 tok/s    16.42 GB
pp4096/tg128          8437.8       22.92   485.4 tok/s    44.0 tok/s      11.349   372.2 tok/s    17.60 GB

Continuous Batching — Same Prompt
pp1024 / tg128 · partial prefix cache hit
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          50.8 tok/s     1.00x   476.7 tok/s   476.7 tok/s      2148.2       4.666
2x          75.6 tok/s     1.49x   495.9 tok/s   247.9 tok/s      4129.6       7.517
4x         102.5 tok/s     2.02x  1440.8 tok/s   360.2 tok/s      2842.6       7.836

Continuous Batching — Different Prompts
pp1024 / tg128 · no cache reuse
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          50.8 tok/s     1.00x   476.7 tok/s   476.7 tok/s      2148.2       4.666
2x          74.4 tok/s     1.46x   502.1 tok/s   251.1 tok/s      4078.6       7.522
4x         101.1 tok/s     1.99x   881.1 tok/s   220.3 tok/s      2589.7       9.711