# CUDA concept and programming

### **Group 5 Members**
- Hernaez, Raeka Estrelle
- Liwanag, Ram Miguel
- Serrano, Paul Rhazzel
- Tiu, Kyle

---
## Project Specifications
[insert project specs]

### Google Colab link
https://colab.research.google.com/drive/1SNLly6QXbylkRBbi87WCoFlog0HELDtE?usp=sharing 

### AI Usage Declaration
[insert ai declaration]

---
## Program Output, Correctness Check, and Execution Time

### C/C++ Program
[insert screenshot]

### CUDA (Variant 2)
[insert screenshot]

### CUDA (Variant 3)
[insert screenshot]

### CUDA (Variant 4)
[insert screenshot]

### CUDA (Variant 5)
[insert screenshot]

---
## NSYS Profiling Results

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
Note: CUDA block sizes (256, 512, and 1024) apply only to the CUDA implementations (not on SIMD). They do not apply to the C, x86-64, XMM, and YMM implementations. All implementations are automatically executed 30 times to obtain their average, minimum, and maximum execution times.

### Table 1. CUDA Block Size: 256
|   | Block size | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|------------|-------------------|-------------------|-------------------|-----------------------|
| C | N/A | 20.0719 ms | 19.2134 ms | 22.3349 | 1.0000x |
| x86-64 | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD XMM | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD YMM | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Unified | 256 | 2.8702 ms | 1.0002 ms |  58.9614 ms | 6.9931x |
| CUDA Prefetch | 256 | 1.0068 ms | 1.0002 ms |  1.0084 ms | 19.9365x |
| CUDA Prefetch+page creation | 256 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	| 256 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |

### Table 2. CUDA Block Size: 512
|   | Block size | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|------------|-------------------|-------------------|-------------------|-----------------------|
| C | N/A | [insert avg] | [insert min] | [insert max] | [insert speedup] |
| x86-64 | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD XMM | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD YMM | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Unified | 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch | 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+page creation | 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	| 512 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |

### Table 3. CUDA Block Size: 1024
|   | Block size | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|------------|-------------------|-------------------|-------------------|-----------------------|
| C | N/A | [insert avg] | [insert min] | [insert max] | [insert speedup] |
| x86-64 | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD XMM | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD YMM | N/A | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
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
