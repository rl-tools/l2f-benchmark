
```
git submodule update --init -- external/rl_tools
```

```
/usr/local/cuda-12/bin/nvcc benchmark.cu -I../../../../../include -use_fast_math --optimize 3 && ./a.out
```