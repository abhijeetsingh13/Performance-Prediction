# Execution-Time
[Steps for running the benchmarks](https://www.spec.org/cpu2017/Docs/runcpu-avoidance.html)

For running any benchmark, first steps till step 9 have to be followed from the above link. 
Go to the directory : cpu-2017/benchspec/CPU
The remaining steps for each benchmark are listed below.

### 500.perlbench_r
- cd 500.perlbench_r/run/run_peak_refrate_perfcount-m64.0000
- ./perlbench_r -I./lib checkspam.pl 2500 5 25 11 150 1 1 1 1 > checkspam.2500.5.25.11.150.1.1.1.1.out 2>> checkspam.2500.5.25.11.150.1.1.1.1.err


