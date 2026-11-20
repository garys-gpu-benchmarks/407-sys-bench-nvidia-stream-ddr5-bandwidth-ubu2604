# Results: 407 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_149 · recorded 2026-11-19). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · Intel(R) Xeon(R) Platinum 8452Y · Ubuntu 26.04.1 LTS · kernel 6.8.0-138-generic · driver 595.112.07
- **Run:** 2026-11-19T21:22:30Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:48 · benchmark 00:11 · whole run 01:07
- **Source:** run 407_20261119_212230
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 368`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 31.8436 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 30.1625 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 31.4421 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 31.0668 |
<!-- /profile:smoke -->
