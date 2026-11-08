# Deep-Dive-CUDA-concept-and-programming

**Group 5 Members**
- Hernaez, Raeka Estrelle
- Liwanag, Ram Miguel
- Serrano, Paul Rhazzel
- Tiu, Kyle

---
## Project Specifications
[insert project specs]

### Google Colab link
[insert Google Colab link here]

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
## NSYS Results

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

### Table 1. CUDA Block Size: 256
|   | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|-------------------|-------------------|-------------------|-----------------------|
| C | [insert avg] | [insert min] | [insert max] | [insert speedup] |
| x86-64 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD XMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD YMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Unified | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+page creation | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |

### Table 2. CUDA Block Size: 512
|   | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|-------------------|-------------------|-------------------|-----------------------|
| C | [insert avg] | [insert min] | [insert max] | [insert speedup] |
| x86-64 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD XMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD YMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Unified | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+page creation | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |

### Table 3. CUDA Block Size: 1024
Each kernel automatically runs 30 times, and the average execution time is recorded below:
|   | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|-------------------|-------------------|-------------------|-----------------------|
| C | [insert avg] | [insert min] | [insert max] | [insert speedup] |
| x86-64 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD XMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD YMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Unified | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+page creation | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |

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

## Project Experience and Insights
[insert problems encountered and solutions made]
[insert unique methodology used] 
[insert AHA moments, etc.]

## Differences between SIMD and SIMT
[discuss, based on your experience on the particular project use case, the differences between SIMD and SIMT in handling parallelism.]
[include also the PROS and CONS of using SIMD and SIMT in your use]
