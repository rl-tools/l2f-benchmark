```
git clone https://github.com/rl-tools/l2f-benchmark
```

```
git submodule update --init -- external/rl_tools
```

```
nvcc benchmark.cu -Iexternal/rl_tools/include -use_fast_math --optimize 3 -std=c++17 && ./a.out
```

Note that the optimal values for `N_BLOCKS`, `N_THREADS` and `N_ITERATIONS` vary depending on your GPU. These values were tuned for the Nvidia T2000 but I got about `20` billion steps per second or ~`6.4` years of simulated time per second on an RTX 4090 (mobile). I believe with better tuning and some other adjustments e.g. in the RK4 integration to reduce register pressure, this could be made much faster, still.