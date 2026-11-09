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
<img width="500" height="204" alt="image" src="https://github.com/user-attachments/assets/8a0babc0-d891-4b26-97d1-b28605dd159b" />


### CUDA (Variant 2)
<img width="500" height="221" alt="image" src="https://github.com/user-attachments/assets/b199e3e0-096c-491b-90b1-ba398f577881" />


### CUDA (Variant 3)
<img width="553" height="217" alt="image" src="https://github.com/user-attachments/assets/6b0fb279-8288-418d-a193-56172ede96c7" />

### CUDA (Variant 4)
[insert screenshot]

### CUDA (Variant 5)
[insert screenshot]

---
## NSYS Profiling Results

### Block Size = 256 
The following screenshots show the NSYS profiling results for all four CUDA variants using a `block size of 256.`

### CUDA (Variant 2)
<img width="790" height="448" alt="image" src="https://github.com/user-attachments/assets/7bdcb066-37f2-4792-9f5e-69bff60d5130" />

### CUDA (Variant 3)
<img width="786" height="454" alt="image" src="https://github.com/user-attachments/assets/3cd0f6bf-85e3-40fe-809d-4c1ee5d18f4b" />

### CUDA (Variant 4)
<img width="829" height="454" alt="image" src="https://github.com/user-attachments/assets/161f8b6f-941b-4eb8-b42d-a8865fdb4ea2" />

### CUDA (Variant 5)
<img width="834" height="450" alt="image" src="https://github.com/user-attachments/assets/1e630306-199c-4d58-8b8f-f5a998284bc6" />

### Block Size = 512 
The following screenshots show the NSYS profiling results for all four CUDA variants using a `block size of 512.`

### CUDA (Variant 2)
[insert nsys screenshot]

### CUDA (Variant 3)
[insert nsys screenshot]

### CUDA (Variant 4)
[insert nsys screenshot]

### CUDA (Variant 5)
[insert nsys screenshot]

### Block Size = 1024 
The following screenshots show the NSYS profiling results for all four CUDA variants using a `block size of 1024.`

### CUDA (Variant 2)
[insert nsys screenshot]

### CUDA (Variant 3)
[insert nsys screenshot]

### CUDA (Variant 4)
[insert nsys screenshot]

### CUDA (Variant 5)
[insert nsys screenshot]

---
## NCU Profiling Results

### CUDA (Variant 2)
[insert nsys screenshot]

### CUDA (Variant 3)
[insert nsys screenshot]

### CUDA (Variant 4)
[insert nsys screenshot]

### CUDA (Variant 5)
[insert nsys screenshot]

---
## Comparative Execution Time
Note: CUDA block sizes (256, 512, and 1024) apply only to the CUDA implementations, not the C or SIMD implementations. The C execution time was taken from Google Colab, while the x86-64, XMM, and YMM execution times were taken from our previously implemented program. All implementations are automatically executed 30 times to obtain their average, minimum, and maximum execution times.

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
