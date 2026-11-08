# Deep-Dive-CUDA-concept-and-programming

**Group 5 Members**
- Hernaez, Raeka Estrelle
- Liwanag, Ram Miguel
- Serrano, Paul Rhazzel
- Tiu, Kyle

### AI Usage Declaration
[insert ai declaration]

---
## Project Specifications
[insert project specs]

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
Each kernel automatically runs 30 times, and the average execution time is recorded below:
| - | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
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
Each kernel automatically runs 30 times, and the average execution time is recorded below:
| - | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
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
| - | Kernel Time (Avg) | Kernel Time (Min) | Kernel Time (Max) | Speedup vs Baseline C |
|---|-------------------|-------------------|-------------------|-----------------------|
| C | [insert avg] | [insert min] | [insert max] | [insert speedup] |
| x86-64 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD XMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| x86-64 SIMD YMM | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Unified | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+page creation | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
| CUDA Prefetch+Page creatition+memadvise	 | [insert avg] | [insert min] |  [insert max] | [insert speedup] |
