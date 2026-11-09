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
| CUDA Unified | 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch | 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+page creation | 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	| 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |

### Table 3. CUDA Block Size: 1024
|   | Block size | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|------------|-------------------|-------------------|-------------------|-----------------------|
| C | N/A | 20.0719 ms | 19.2134 ms | 22.3349 ms | 1.0000x |
| x86-64 | N/A | 10.3671 ms | 9.5470 ms | 13.4715 ms | 1.9369x |
| x86-64 SIMD XMM | N/A | 10.3294 ms | 9.0370 ms | 13.0426 ms | 1.9439x |
| x86-64 SIMD YMM | N/A | 9.1923 ms | 8.8670 ms | 9.6287 ms | 2.1836x |
| CUDA Unified | 1024 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch | 1024 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+page creation | 1024 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	| 1024 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |

---
## Analysis of Results 
### Analysis of kernel execution time
[insert answer]

### Analysis of speed performance across all platforms
[insert answer]

### Additional (from the specs)
--Guide questions for analysis (for all CUDA variants).  This is not comprehensive; add more analysis as necessary --

- a.) How does block size affect execution time (observing various elements and using max blocks)?  Which block size will you recommend?
- b.) Is prefetching always recommended, or should CUDA manage memory?  Give some use cases in which one is better than the other.
- c.) Between SIMD and SIMT, which one is faster? Give some use cases in which one is better than the other.
  
---
## Project Experience and Insights
- [insert problems encountered and solutions made]
- [insert unique methodology used] 
- [insert AHA moments, etc.]
  
---
## Differences between SIMD and SIMT
- [discuss, based on your experience on the particular project use case, the differences between SIMD and SIMT in handling parallelism.]
- [include also the PROS and CONS of using SIMD and SIMT in your use]
