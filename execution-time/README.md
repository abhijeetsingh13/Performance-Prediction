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

### 508.namd_r
- cd 508.namd_r/run/run_peak_refrate_perfcount-m64.0000
- ./namd_r --input apoa1.input --output apoa1.ref.output --iterations 65 > namd.out 2>> namd.err

### 510.parest_r
- cd 510.parest_r/run/run_peak_refrate_perfcount-m64.0000
- ./parest_r ref.prm > ref.out 2>> ref.err

### 511.povray_r
- cd 511.povray_r/run/run_peak_refrate_perfcount-m64.0000
- ./povray_r SPEC-benchmark-ref.ini > SPEC-benchmark-ref.stdout 2>> SPEC-benchmark-ref.stderr

### 519.lbm_r
- cd 519.lbm_r/run/run_peak_refrate_perfcount-m64.0000
- ./lbm_r 3000 reference.dat 0 0 100_100_130_ldc.of > lbm.out 2>> lbm.err

### 520.omnetpp_r
- cd 520.omnetpp_r/run/run_peak_refrate_perfcount-m64.0000
- ./omnetpp_r -c General -r 0 > omnetpp.General-0.out 2>> omnetpp.General-0.err

### 521.wrf_r
- cd 521.wrf_r/run/run_base_refrate_perfcount-m64.0000
- ./wrf_r > rsl.out.0000 2>> wrf.err

### 523.xalancbmk_r
- cd 523.xalancbmk_r/run/run_peak_refrate_perfcount-m64.0000
- ./cpuxalan_r -v t5.xml xalanc.xsl > ref-t5.out 2>> ref-t5.err

### 525.x264_r
- cd 525.x264_r/run/run_peak_refrate_perfcount-m64.0000
- ./x264_r --pass 1 --stats x264_stats.log --bitrate 1000 --frames 1000 -o BuckBunny_New.264 BuckBunny.yuv 1280x720 > run_000-1000_x264_r_x264_pass1.out 2>> run_000-1000_x264_r_x264_pass1.err
- ./x264_r --pass 2 --stats x264_stats.log --bitrate 1000 --dumpyuv 200 --frames 1000 -o BuckBunny_New.264 BuckBunny.yuv 1280x720 > run_000-1000_x264_r_x264_pass2.out 2>> run_000-1000_x264_r_x264_pass2.err
- ./x264_r --seek 500 --dumpyuv 200 --frames 1250 -o BuckBunny_New.264 BuckBunny.yuv 1280x720 > run_0500-1250_x264_r_x264.out 2>> run_0500-1250_x264_r_x264.err

### 526.blender_r
- cd 526.blender_r/run/run_peak_refrate_perfcount-m64.0000
- ./blender_r sh3_no_char.blend --render-output sh3_no_char_ --threads 1 -b -F RAWTGA -s 849 -e 849 -a > sh3_no_char.849.spec.out 2>> sh3_no_char.849.spec.err

### 527.cam4_r
- cd 527.cam4_r/run/run_base_refrate_perfcount-m64.0000
- ./cam4_r > cam4_r.txt 2>> cam4_r.err

### 531.deepsjeng_r
- cd 531.deepsjeng_r/run/run_peak_refrate_perfcount-m64.0000
- ./deepsjeng_r ref.txt > ref.out 2>> ref.err

### 538.imagick_r
- cd 538.imagick_r/run/run_peak_refrate_perfcount-m64.0000
- ./imagick_r -limit disk 0 refrate_input.tga -edge 41 -resample 181% -emboss 31 -colorspace YUV -mean-shift 19x19+15% -resize 30% time refrate_output.tga > refrate_convert.out 2>> refrate_convert.err

### 541.leela_r
- cd 541.leela_r/run/run_peak_refrate_perfcount-m64.0000
- ./leela_r ref.sgf > ref.out 2>> ref.err

### 548.exchange2_r
- cd 548.exchange2_r/run/run_peak_refrate_perfcount-m64.0000
- ./exchange2_r 6 > exchange2.txt 2>> exchange2.err

### 549.fotonik3d_r
- cd 549.fotonik3d_r/run/run_peak_refrate_perfcount-m64.0000
- ./fotonik3d_r > fotonik3d_r.log 2>> fotonik3d_r.err

### 554.roms_r
- cd 554.roms_r/run/run_peak_refrate_perfcount-m64.0000
- ./roms_r < ocean_benchmark2.in.x > ocean_benchmark2.log 2>> ocean_benchmark2.err

### 557.xz_r
- cd 557.xz_r/run/run_peak_refrate_perfcount-m64.0000
- ./xz_r cld.tar.xz 160 19cf30ae51eddcbefda78dd06014b4b96281456e078ca7c13e1c0c9e6aaea8dff3efb4ad6b0456697718cede6bd5454852652806a657bb56e07d61128434b474 59796407 61004416 6 > cld.tar-160-6.out 2>> cld.tar-160-6.err
- ./xz_r cpu2006docs.tar.xz 250 055ce243071129412e9dd0b3b69a21654033a9b723d874b2015c774fac1553d9713be561ca86f74e4f16f22e664fc17a79f30caa5ad2c04fbc447549c2810fae 23047774 23513385 6e > cpu2006docs.tar-250-6e.out 2>> cpu2006docs.tar-250-6e.err
- ./xz_r input.combined.xz 250 a841f68f38572a49d86226b7ff5baeb31bd19dc637a922a972b2e6d1257a890f6a544ecab967c313e370478c74f760eb229d4eef8a8d2836d233d3e9dd1430bf 40401484 41217675 7 > input.combined-250-7.out 2>> input.combined-250-7.err