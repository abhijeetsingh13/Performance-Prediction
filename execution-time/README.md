# Execution-Time
[Steps for running the benchmarks](https://www.spec.org/cpu2017/Docs/runcpu-avoidance.html)

For running any benchmark, first steps till step 9 have to be followed from the above link. 
Go to the directory : cpu-2017/benchspec/CPU
The remaining steps for each benchmark are listed below.

### 500.perlbench_r
- cd 500.perlbench_r/run/run_peak_refrate_perfcount-m64.0000
- ./perlbench_r -I./lib checkspam.pl 2500 5 25 11 150 1 1 1 1 > checkspam.2500.5.25.11.150.1.1.1.1.out 2>> checkspam.2500.5.25.11.150.1.1.1.1.err
- ./perlbench_r -I./lib diffmail.pl 4 800 10 17 19 300 > diffmail.4.800.10.17.19.300.out 2>> diffmail.4.800.10.17.19.300.err
- ./perlbench_r -I./lib splitmail.pl 6400 12 26 16 100 0 > splitmail.6400.12.26.16.100.0.out 2>> splitmail.6400.12.26.16.100.0.err

### 502.gcc_r
- cd 502.gcc_r/run/run_peak_refrate_perfcount-m64.0000
- ./cpugcc_r gcc-pp.c -O3 -finline-limit=0 -fif-conversion -fif-conversion2 -o gcc-pp.opts-O3_-finline-limit_0_-fif-conversion_-fif-conversion2.s > gcc-pp.opts-O3_-finline-limit_0_-fif-conversion_-fif-conversion2.out 2>> gcc-pp.opts-O3_-finline-limit_0_-fif-conversion_-fif-conversion2.err
- ./cpugcc_r gcc-pp.c -O2 -finline-limit=36000 -fpic -o gcc-pp.opts-O2_-finline-limit_36000_-fpic.s > gcc-pp.opts-O2_-finline-limit_36000_-fpic.out 2>> gcc-pp.opts-O2_-finline-limit_36000_-fpic.err
- ./cpugcc_r gcc-smaller.c -O3 -fipa-pta -o gcc-smaller.opts-O3_-fipa-pta.s > gcc-smaller.opts-O3_-fipa-pta.out 2>> gcc-smaller.opts-O3_-fipa-pta.err
- ./cpugcc_r ref32.c -O5 -o ref32.opts-O5.s > ref32.opts-O5.out 2>> ref32.opts-O5.err

### 503.bwaves_r
- cd 503.bwaves_r/run/run_base_refrate_perfcount-m64.0000
- ./bwaves_r bwaves_1 < bwaves_1.in > bwaves_1.out 2>> bwaves_1.err
- ./bwaves_r bwaves_2 < bwaves_2.in > bwaves_2.out 2>> bwaves_2.err
- ./bwaves_r bwaves_3 < bwaves_3.in > bwaves_3.out 2>> bwaves_3.err
- ./bwaves_r bwaves_4 < bwaves_4.in > bwaves_4.out 2>> bwaves_4.err

### 505.mcf_r
- cd 505.mcf_r/run/run_peak_refrate_perfcount-m64.0000
- ./mcf_r inp.in  > inp.out 2>> inp.err

### 507.cactuBSSN_r
- cd 507.cactuBSSN_r/run/run_peak_refrate_perfcount-m64.0000
- ./cactusBSSN_r spec_ref.par   > spec_ref.out 2>> spec_ref.err


