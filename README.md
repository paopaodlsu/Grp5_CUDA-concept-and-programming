# CUDA concept and programming

### **Group 5 Members**
- Hernaez, Raeka Estrelle
- Liwanag, Ram Miguel
- Serrano, Paul Rhazzel
- Tiu, Kyle

---
## Project Specifications
#### Objective: 
Implement the vector triad operation using C, x86-64 assembly, SIMD XMM, and SIMD YMM.

#### Input: 
A scalar variable n representing the vector length. Vectors B, C, and D contain single-precision floating-point values.

#### Process:
*A[i] = B[i] + C[i] x D[i]*

#### Output: 
Store the computed results in vector A. Display the execution time, first five elements, and last five elements of vector A for verification.

#### Requirements:
* Implement four versions of the vector triad operation: C, x86-64 assembly, SIMD XMM, and SIMD YMM.
* Test vector sizes of 2<sup>20</sup>, 2<sup>26</sup>, and 2<sup>28</sup>. If 2<sup>30</sup> is not possible, reduce the size to 2<sup>28</sup> or 2<sup>29</sup>, depending on memory capacity.
* Execute each kernel at least 30 times and obtain the average execution time.
* Test boundary elements to verify that the SIMD implementations handle vector sizes that are not exact multiples of the register width.

### Google Colab link
https://colab.research.google.com/drive/1SNLly6QXbylkRBbi87WCoFlog0HELDtE?usp=sharing 

### AI Usage Declaration
[insert ai declaration]

---
## Program Output, Correctness Check, and Execution Time


### C/C++ Program
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/8a0babc0-d891-4b26-97d1-b28605dd159b" />

### Block Size = 256 

#### CUDA (Variant 2)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/b199e3e0-096c-491b-90b1-ba398f577881" />

#### CUDA (Variant 3)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/6b0fb279-8288-418d-a193-56172ede96c7" />

#### CUDA (Variant 4)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/4ccac663-8eb3-43f5-a394-4f9c44f0a04c" />

#### CUDA (Variant 5)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/64a239ca-93b8-4cb1-abae-af41bb02980b" />


### Block Size = 512 

#### CUDA (Variant 2)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/5e6ba299-40ef-4c9f-b0ef-52bb399deb47" />

#### CUDA (Variant 3)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/5803199d-b607-4b92-92cf-74efddf8b594" />

#### CUDA (Variant 4)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/80052d17-95ec-44bd-8481-790d3155cb11" />

#### CUDA (Variant 5)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/3b69c280-d934-4dcf-b1ee-40315a3fcb1b" />

### Block Size = 1024

#### CUDA (Variant 2)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/cb1c390d-35cd-4fa6-8f77-b49c2209224b" />

#### CUDA (Variant 3)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/0c12fff6-1e9a-4601-b4e0-6a6a8b24d168" />

#### CUDA (Variant 4)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/09338e71-4f99-4857-95a9-4c98ff1238a4" />

#### CUDA (Variant 5)
<img width="550" height="270" alt="image" src="https://github.com/user-attachments/assets/32f2c03f-278d-4819-8c64-ca344b4c193c" />


---
## NSYS Profiling Results

### Block Size = 256 
The following screenshots show the NSYS profiling results for all four CUDA variants using a `block size of 256.`

### CUDA (Variant 2)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/7bdcb066-37f2-4792-9f5e-69bff60d5130" />

### CUDA (Variant 3)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/3cd0f6bf-85e3-40fe-809d-4c1ee5d18f4b" />

### CUDA (Variant 4)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/161f8b6f-941b-4eb8-b42d-a8865fdb4ea2" />

### CUDA (Variant 5)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/1e630306-199c-4d58-8b8f-f5a998284bc6" />

### Block Size = 512 
The following screenshots show the NSYS profiling results for all four CUDA variants using a `block size of 512.`

### CUDA (Variant 2)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/11e840b5-82f9-4de0-aec2-e0cb50894801" />

### CUDA (Variant 3)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/abc82f6a-c1cd-4d7d-9932-c83e6da5127e" />

### CUDA (Variant 4)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/0f64e478-f0ec-458b-8a7a-98a5cb8eeed7" />

### CUDA (Variant 5)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/9291b78b-f0f4-47af-8ac5-8c7516d6fc74" />


### Block Size = 1024 
The following screenshots show the NSYS profiling results for all four CUDA variants using a `block size of 1024.`

### CUDA (Variant 2)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/f7b33387-5eff-48fd-9d75-b4bbe13c08cf" />

### CUDA (Variant 3)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/aabcd173-bc39-49dc-a706-1db4e9211fd1" />

### CUDA (Variant 4)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/7aa8131f-b22b-406b-b9ca-787d3a4fcac2" />

### CUDA (Variant 5)
<img width="1000" height="700" alt="image" src="https://github.com/user-attachments/assets/b36f9122-5c4f-4fc2-9764-28d7e6b1eedb" />


---
## NCU Profiling Results

### Block Size = 256 

#### CUDA (Variant 2)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/bae5c148-deff-4f8f-981b-04d897b00e6d" />

#### CUDA (Variant 3)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/8236c462-5db3-4d68-a56a-2818322119e4" />

#### CUDA (Variant 4)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/7c790ce2-c7a7-42f5-8469-4b9714049f21" />

#### CUDA (Variant 5)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/a306581b-4b58-474b-9b69-9b754924b970" />


### Block Size = 512 

#### CUDA (Variant 2)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/fbbc989b-cfd5-4a44-ae2d-1fd81b39e86f" />

#### CUDA (Variant 3)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/c0b09041-165a-4fe7-a946-032e1038f95d" />

#### CUDA (Variant 4)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/7a483b66-1ebb-412d-b12c-5f7a1dad9017" />

#### CUDA (Variant 5)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/2f5ee86e-eecf-4768-93f2-d869e345f937" />


### Block Size = 1024 

#### CUDA (Variant 2)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/3c5e7821-ab8e-4f7c-9fa2-b87028885412" />

#### CUDA (Variant 3)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/e3df2152-b890-4a74-af23-fd7880e336c6" />

#### CUDA (Variant 4)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/0787044d-9eca-47f8-948a-49f8a13f8621" />

#### CUDA (Variant 5)
<img width="560" height="458" alt="image" src="https://github.com/user-attachments/assets/8763cf68-f527-463a-a67f-4ebed2973f37" />


---
## Comparative Execution Time
Note: CUDA block sizes (256, 512, and 1024) apply only to the CUDA implementations, not the C or SIMD implementations. The C execution time was taken from Google Colab, while the x86-64, XMM, and YMM execution times were taken from our previously implemented program. All implementations are automatically executed 30 times to obtain their average, minimum, and maximum execution times.

### 2<sup>24</sup> elements
 
### Table 1. CUDA Block Size: 256
|   | Block size | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|------------|-------------------|-------------------|-------------------|-----------------------|
| C | N/A | 20.0719 ms | 19.2134 ms | 22.3349 ms | 1.0000x |
| x86-64 | N/A | 10.3671 ms | 9.5470 ms | 13.4715 ms | 1.9369x |
| x86-64 SIMD XMM | N/A | 10.3294 ms | 9.0370 ms | 13.0426 ms | 1.9439x |
| x86-64 SIMD YMM | N/A | 9.1923 ms | 8.8670 ms | 9.6287 ms | 2.1836x |
| CUDA Unified | 256 | 2.8702 ms | 1.0002 ms |  58.9614 ms | 6.9931x |
| CUDA Prefetch | 256 | 1.0068 ms | 1.0002 ms |  1.0084 ms | 19.9365x |
| CUDA Prefetch+page creation | 256 | 1.0003 ms | 0.9981 ms | 1.0008 ms | 20.0668x |
| CUDA Prefetch+Page creatition+memadvise	| 256 | 1.0004 ms | 0.9981 ms | 1.0011 ms | 20.0639x |

With a block size of 256, all eight implementations produced correct results, with no errors reported. YMM performed best among the CPU implementations, while the CUDA versions with prefetching had noticeably lower average kernel times than the version without prefetching. CUDA Prefetch + Page Creation recorded the lowest average kernel time at 1.0003 ms, followed closely by the version with MemAdvise at 1.0004 ms.

### Table 2. CUDA Block Size: 512
|   | Block size | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|------------|-------------------|-------------------|-------------------|-----------------------|
| C | N/A | 20.0719 ms | 19.2134 ms | 22.3349 ms | 1.0000x |
| x86-64 | N/A | 10.3671 ms | 9.5470 ms | 13.4715 ms | 1.9369x |
| x86-64 SIMD XMM | N/A | 10.3294 ms | 9.0370 ms | 13.0426 ms | 1.9439x |
| x86-64 SIMD YMM | N/A | 9.1923 ms | 8.8670 ms | 9.6287 ms | 2.1836x |
| CUDA Unified | 512 | 2.9957 ms | 1.0078 ms |  62.6203 ms | 6.6998x |
| CUDA Prefetch | 512 | 1.0082 ms | 1.0065 ms | 1.0094 ms | 19.9089x |
| CUDA Prefetch+page creation | 512 | 1.0081 ms | 1.0063 ms | 1.0088 ms | 19.9101x |
| CUDA Prefetch+Page creatition+memadvise	| 512 | 1.0081 ms | 1.0064 ms | 1.0087 ms | 19.9108x |

At block size 512, all implementations passed the correctness check. The three CUDA variants that use prefetching recorded very similar average kernel times, all around 1.008 ms. Variant 4 was slightly faster than Variant 3 in this run, while Variant 5 had the lowest minimum time. 

### Table 3. CUDA Block Size: 1024
|   | Block size | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|------------|-------------------|-------------------|-------------------|-----------------------|
| C | N/A | 20.0719 ms | 19.2134 ms | 22.3349 ms | 1.0000x |
| x86-64 | N/A | 10.3671 ms | 9.5470 ms | 13.4715 ms | 1.9369x |
| x86-64 SIMD XMM | N/A | 10.3294 ms | 9.0370 ms | 13.0426 ms | 1.9439x |
| x86-64 SIMD YMM | N/A | 9.1923 ms | 8.8670 ms | 9.6287 ms | 2.1836x |
| CUDA Unified | 1024 | 2.9112 ms] | 1.0222 ms | 59.5637 ms | 6.8948x |
| CUDA Prefetch | 1024 | 1.0614 ms | 1.0600 ms | 1.0625 ms | 18.9105x |
| CUDA Prefetch+page creation | 1024 | 1.0616 ms | 1.0603 ms | 1.0628 | 18.9073x |
| CUDA Prefetch+Page creatition+memadvise	| 1024 | 1.0614 ms | 1.0601 ms | 1.0626 ms | 18.9101x |

The 1024 block size results show that all implementations passed the correctness check. The prefetching implementations recorded similar average execution times of around 1.06 ms, while the CUDA version without prefetching had a noticeably higher maximum execution time. 

---
## Analysis of Results 
### Analysis of kernel execution time
Among CPU implementations, the scalar C baseline was slowest at 20.07 ms, while x86-64 assembly with 10.37 ms and XMM 10.33 ms were nearly identical, and YMM was fastest at 9.19 ms. This near-tie suggests the CPU kernels are memory-bandwidth-limited, since each element requires three loads and one store per multiply-add. The CUDA kernels were much faster, at about 1.00 to 1.06 ms, implying roughly 268 GB/s effective bandwidth for 2^24 floats across four arrays. CUDA Unified averaged 2.87 ms at block size 256, but its minimum matched the prefetch variants, while the maximum of about 59 ms reflects first-launch page-fault migration. Page creation and cudaMemAdvise made no measurable difference, as Variants 3, 4, and 5 were within 0.1% of each other at every block size.

### Analysis of speed performance across all platforms
For the speed performance, the C baseline, x86-64 and XMM reached about 1.94x, YMM reached 2.18x, CUDA Unified about 7x, and prefetched CUDA variants about 20x at block size 256. Against the best CPU result, the prefetched CUDA kernels were about 9x faster, consistent with the GPU’s much higher memory bandwidth. Widening SIMD from 128-bit to 256-bit gained only about 11%, as the CPU is already close to saturating its memory bus. However, these comparisons should be interpreted carefully because the C execution time came from Google Colab, while the assembly and SIMD execution times came from our previously implemented program on different hardware. Furthermore, the measured kernel times exclude host-to-device memory transfers, meaning that including these transfers in the total execution time would reduce the CUDA advantage, particularly for one-time operations involving smaller datasets.

### Additional Analysis
Block size directly influences CUDA execution time because it determines how many threads are grouped together within each block, affecting GPU occupancy and resource utilization. Based on our results, a block size of 256 performed the best, achieving approximately 1.0003 ms with prefetching and page creation, compared to 1.0081 ms at 512 and 1.0616 ms at 1024. This indicates that increasing the block size does not necessarily improve performance, since larger blocks may affect resource allocation and reduce the number of blocks that can execute concurrently. Regarding memory management, prefetching is not always recommended because CUDA Unified Memory can automatically manage data migration between the CPU and GPU, making it more convenient for applications with unpredictable memory access patterns. However, explicit prefetching is more beneficial when processing large datasets with predictable access patterns because it allows data migration to occur before the kernel requires the data, reducing potential memory migration delays.
  
---
## Project Experience and Insights
One of the main challenges we encountered during the project was experiencing difficulties accessing the GPU runtime in Google Colab, as the platform kept restricting when it was executing the CUDA, causing a delay on addressing it first before proceeding to continue with the experiment which was waiting around the runtime to clear. Another challenge was comparing the performance of different implementations while ensuring that each produced correct and consistent results. This has been addressed this by executing each implementation 30 times and recording the average, minimum, and maximum execution times to provide a more reliable performance comparison. An important part of the methodology was testing different CUDA block sizes and memory management variants to determine how they affected kernel performance. An "AHA" moment was finding that GPU acceleration alone does not automatically guarantee optimal performance, since memory management and thread configuration also have a significant impact on execution time. Through the creation of this project, it has given a clearer and better understanding of how parallel computing techniques work and how selecting the appropriate implementation and configuration can significantly improve computational performance.
  
---
## Differences between SIMD and SIMT
Based on our vector triad operation, SIMD and SIMT both utilize parallelism however it has a difference in how they process multiple data elements. SIMD executes a single instruction on multiple data values simultaneously, as demonstrated by our XMM and YMM implementations, where YMM achieved a better performance than XMM because of its wider 256-bit registers. In contrast, SIMT distributes individual threads across GPU processing units, allowing a large number of threads to execute similar instructions on different data elements simultaneously. The main advantage of SIMD is its efficient execution of parallel operations directly on the CPU without requiring GPU memory transfers, although its parallel processing capacity is limited by the CPU's available vector registers and resources. Meanwhile, SIMT provides greater parallel processing capabilities for large datasets, as demonstrated by the produced CUDA results, but it requires careful management of memory transfers, thread configurations, and GPU resources to achieve optimal performance.
