# Results: 407 STREAM - CPU (Copy/Scale/Add/Triad)

**Main goal:** Measure sustained CPU STREAM bandwidth  
**Tools:** Compile src/stream.c with gcc -O3 -fopenmp and run build/stream

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_145 · recorded 2026-11-17). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · AMD EPYC 9374F 32-Core Processor · Ubuntu 26.04.1 LTS · kernel 6.8.0-138-generic · driver 595.112.07
- **Run:** 2026-11-17T10:55:30Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:24 · benchmark 00:00 · whole run 00:30
- **Source:** run 407_20261117_105530
- **Command:** `bash run_benchmark.sh --smoke --numa-node 0 --num-threads 4 --thread-affinity core --array-size 10000000 --num-iterations 2`

| # | Metric | Result |
|---|---|---|
| 1 | Best Copy bandwidth, GB/s (copy_bandwidth_gb_s) | 56.6487 |
| 2 | Best Scale bandwidth, GB/s (scale_bandwidth_gb_s) | 55.8836 |
| 3 | Best Add bandwidth, GB/s (add_bandwidth_gb_s) | 56.5911 |
| 4 | Best Triad bandwidth, GB/s (triad_bandwidth_gb_s) | 56.7659 |
<!-- /profile:smoke -->
