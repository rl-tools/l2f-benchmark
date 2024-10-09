```
git clone https://github.com/rl-tools/l2f-benchmark
```

```
git submodule update --init -- external/rl_tools
```

```
nvcc benchmark.cu -I../../../../../include -use_fast_math --optimize 3 && ./a.out
```