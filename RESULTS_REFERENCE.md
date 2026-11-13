# Results: 407 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 80GB HBM3 (81559 MiB) · Intel(R) Xeon(R) Platinum 8470 · Ubuntu 26.04.1 LTS · kernel 6.8.0-147-generic · driver 595.91.07
- **Run:** 2026-11-12T22:45:58Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:34 · benchmark 00:01 · whole run 00:43
- **Source:** run 407_20261112_224558
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 2`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 45.9804 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 39.4239 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 44.067099999999996 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 43.4859 |
<!-- /profile:smoke -->
