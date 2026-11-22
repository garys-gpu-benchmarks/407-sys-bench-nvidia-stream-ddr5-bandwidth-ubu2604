# Results: 407 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results from the validation run on the system shown in each section (recorded 2026-11-22). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 80GB HBM3 (81559 MiB) · Intel(R) Xeon(R) Platinum 8468 · Ubuntu 26.04.1 LTS · kernel 6.8.0-149-generic · driver 595.112.07
- **Run:** 2026-11-22T10:55:23Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:37 · benchmark 00:10 · whole run 00:53
- **Source:** run 407_20261122_105523
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 368`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 53.4392 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 33.2032 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 37.8184 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 38.5157 |
<!-- /profile:smoke -->
