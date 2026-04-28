oMLX - LLM inference, optimized for your Mac
https://github.com/jundot/omlx
Benchmark Model: Qwen3-Coder-30B-A3B-Instruct-MLX-4bit
================================================================================

Single Request Results
--------------------------------------------------------------------------------
Test                TTFT(ms)    TPOT(ms)        pp TPS        tg TPS      E2E(s)    Throughput    Peak Mem
pp1024/tg128          1746.7       13.43   586.3 tok/s    75.0 tok/s       3.453   333.7 tok/s    16.59 GB
pp4096/tg128          6935.4       16.85   590.6 tok/s    59.8 tok/s       9.075   465.4 tok/s    17.06 GB

Continuous Batching — Same Prompt
pp1024 / tg128 · partial prefix cache hit
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          75.0 tok/s     1.00x   586.3 tok/s   586.3 tok/s      1746.7       3.453
2x         100.7 tok/s     1.34x   581.8 tok/s   290.9 tok/s      3519.9       6.062
4x         122.8 tok/s     1.64x  2269.7 tok/s   567.4 tok/s      1804.5       5.975

Continuous Batching — Different Prompts
pp1024 / tg128 · no cache reuse
--------------------------------------------------------------------------------
Batch           tg TPS   Speedup        pp TPS    pp TPS/req    TTFT(ms)      E2E(s)
1x          75.0 tok/s     1.00x   586.3 tok/s   586.3 tok/s      1746.7       3.453
2x          99.8 tok/s     1.33x   587.9 tok/s   293.9 tok/s      3483.4       6.050