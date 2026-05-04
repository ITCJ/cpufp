# Qualcomm Snapdragon 8 Gen5

Architecture: Third Generation Oryon

Setting: 6 Performance cores @ 3.32Ghz + 2 Prime cores @ 3.8Ghz

For single Performance core:

<pre>
$ ./cpufp --thread_pool=[0]
Number Threads: 1
Thread Pool Binding: 0
----------------------------------------------------------------
| Instruction Set | Core Computation        | Peak Performance |
| i8mm            | mmla(s32,s8,s8)         | 423 GOPS         |
| i8mm            | mmla(u32,u8,u8)         | 422.96 GOPS      |
| i8mm            | mmla(s32,u8,s8)         | 420.8 GOPS       |
| i8mm            | dp4a.vs(s32,s8,u8)      | 211.61 GOPS      |
| i8mm            | dp4a.vs(s32,u8,s8)      | 211.9 GOPS       |
| i8mm            | dp4a.vv(s32,u8,s8)      | 210.24 GOPS      |
| asimd_dp        | dp4a.vs(s32,s8,s8)      | 211.26 GOPS      |
| asimd_dp        | dp4a.vv(s32,s8,s8)      | 211.8 GOPS       |
| asimd_dp        | dp4a.vs(u32,u8,u8)      | 211.88 GOPS      |
| asimd_dp        | dp4a.vv(u32,u8,u8)      | 211.76 GOPS      |
| bf16            | mmla(f32,bf16,bf16)     | 105.86 GFLOPS    |
| bf16            | dp2a.vs(f32,bf16,bf16)  | 105.95 GFLOPS    |
| bf16            | dp2a.vv(f32,bf16,bf16)  | 105.83 GFLOPS    |
| asimd_hp        | fmla.vs(fp16,fp16,fp16) | 105.92 GFLOPS    |
| asimd_hp        | fmla.vv(fp16,fp16,fp16) | 105.85 GFLOPS    |
| asimd           | fmla.vs(f32,f32,f32)    | 52.943 GFLOPS    |
| asimd           | fmla.vv(f32,f32,f32)    | 52.925 GFLOPS    |
| asimd           | fmla.vs(f64,f64,f64)    | 26.136 GFLOPS    |
| asimd           | fmla.vv(f64,f64,f64)    | 26.439 GFLOPS    |
----------------------------------------------------------------
</pre>

For 6 Performance cores:

<pre>
$ ./cpufp --thread_pool=[0-5]
Number Threads: 6
Thread Pool Binding: 0 1 2 3 4 5
----------------------------------------------------------------
| Instruction Set | Core Computation        | Peak Performance |
| i8mm            | mmla(s32,s8,s8)         | 2.5253 TOPS      |
| i8mm            | mmla(u32,u8,u8)         | 2.5278 TOPS      |
| i8mm            | mmla(s32,u8,s8)         | 2.4928 TOPS      |
| i8mm            | dp4a.vs(s32,s8,u8)      | 1.2405 TOPS      |
| i8mm            | dp4a.vs(s32,u8,s8)      | 1.2672 TOPS      |
| i8mm            | dp4a.vv(s32,u8,s8)      | 1.2497 TOPS      |
| asimd_dp        | dp4a.vs(s32,s8,s8)      | 1.2594 TOPS      |
| asimd_dp        | dp4a.vv(s32,s8,s8)      | 1.2597 TOPS      |
| asimd_dp        | dp4a.vs(u32,u8,u8)      | 1.2571 TOPS      |
| asimd_dp        | dp4a.vv(u32,u8,u8)      | 1.2525 TOPS      |
| bf16            | mmla(f32,bf16,bf16)     | 628.01 GFLOPS    |
| bf16            | dp2a.vs(f32,bf16,bf16)  | 631.85 GFLOPS    |
| bf16            | dp2a.vv(f32,bf16,bf16)  | 633.1 GFLOPS     |
| asimd_hp        | fmla.vs(fp16,fp16,fp16) | 630.53 GFLOPS    |
| asimd_hp        | fmla.vv(fp16,fp16,fp16) | 630.63 GFLOPS    |
| asimd           | fmla.vs(f32,f32,f32)    | 313.55 GFLOPS    |
| asimd           | fmla.vv(f32,f32,f32)    | 313.94 GFLOPS    |
| asimd           | fmla.vs(f64,f64,f64)    | 158.02 GFLOPS    |
| asimd           | fmla.vv(f64,f64,f64)    | 158.28 GFLOPS    |
----------------------------------------------------------------
</pre>

For single Prime core:

<pre>
$ ./cpufp --thread_pool=[6]
Number Threads: 1
Thread Pool Binding: 6
----------------------------------------------------------------
| Instruction Set | Core Computation        | Peak Performance |
| i8mm            | mmla(s32,s8,s8)         | 970.27 GOPS      |
| i8mm            | mmla(u32,u8,u8)         | 970.49 GOPS      |
| i8mm            | mmla(s32,u8,s8)         | 970.84 GOPS      |
| i8mm            | dp4a.vs(s32,s8,u8)      | 485.41 GOPS      |
| i8mm            | dp4a.vs(s32,u8,s8)      | 485.35 GOPS      |
| i8mm            | dp4a.vv(s32,u8,s8)      | 485.38 GOPS      |
| asimd_dp        | dp4a.vs(s32,s8,s8)      | 485.39 GOPS      |
| asimd_dp        | dp4a.vv(s32,s8,s8)      | 485.26 GOPS      |
| asimd_dp        | dp4a.vs(u32,u8,u8)      | 485.39 GOPS      |
| asimd_dp        | dp4a.vv(u32,u8,u8)      | 485.32 GOPS      |
| bf16            | mmla(f32,bf16,bf16)     | 238.75 GFLOPS    |
| bf16            | dp2a.vs(f32,bf16,bf16)  | 242.69 GFLOPS    |
| bf16            | dp2a.vv(f32,bf16,bf16)  | 242.68 GFLOPS    |
| asimd_hp        | fmla.vs(fp16,fp16,fp16) | 241.67 GFLOPS    |
| asimd_hp        | fmla.vv(fp16,fp16,fp16) | 242.65 GFLOPS    |
| asimd           | fmla.vs(f32,f32,f32)    | 121.32 GFLOPS    |
| asimd           | fmla.vv(f32,f32,f32)    | 121.34 GFLOPS    |
| asimd           | fmla.vs(f64,f64,f64)    | 60.594 GFLOPS    |
| asimd           | fmla.vv(f64,f64,f64)    | 60.673 GFLOPS    |
----------------------------------------------------------------
</pre>

For 2 Prime cores:

<pre>
$ ./cpufp --thread_pool=[6,7]
Number Threads: 2
Thread Pool Binding: 6 7
----------------------------------------------------------------
| Instruction Set | Core Computation        | Peak Performance |
| i8mm            | mmla(s32,s8,s8)         | 1.7548 TOPS      |
| i8mm            | mmla(u32,u8,u8)         | 1.7497 TOPS      |
| i8mm            | mmla(s32,u8,s8)         | 1.7424 TOPS      |
| i8mm            | dp4a.vs(s32,s8,u8)      | 877.86 GOPS      |
| i8mm            | dp4a.vs(s32,u8,s8)      | 878.05 GOPS      |
| i8mm            | dp4a.vv(s32,u8,s8)      | 878.12 GOPS      |
| asimd_dp        | dp4a.vs(s32,s8,s8)      | 874.96 GOPS      |
| asimd_dp        | dp4a.vv(s32,s8,s8)      | 877.98 GOPS      |
| asimd_dp        | dp4a.vs(u32,u8,u8)      | 878.06 GOPS      |
| asimd_dp        | dp4a.vv(u32,u8,u8)      | 878 GOPS         |
| bf16            | mmla(f32,bf16,bf16)     | 433.63 GFLOPS    |
| bf16            | dp2a.vs(f32,bf16,bf16)  | 437.46 GFLOPS    |
| bf16            | dp2a.vv(f32,bf16,bf16)  | 433.07 GFLOPS    |
| asimd_hp        | fmla.vs(fp16,fp16,fp16) | 438.87 GFLOPS    |
| asimd_hp        | fmla.vv(fp16,fp16,fp16) | 438.5 GFLOPS     |
| asimd           | fmla.vs(f32,f32,f32)    | 219.46 GFLOPS    |
| asimd           | fmla.vv(f32,f32,f32)    | 219.49 GFLOPS    |
| asimd           | fmla.vs(f64,f64,f64)    | 108.57 GFLOPS    |
| asimd           | fmla.vv(f64,f64,f64)    | 109.75 GFLOPS    |
----------------------------------------------------------------
</pre>

