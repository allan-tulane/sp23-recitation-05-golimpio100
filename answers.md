# CMPS 2200 Recitation 5
## Answers

**Name:** Griffin Olimpio and Devin Gutierrez


Place all written answers from `recitation-06.md` here for easier grading.







- **1b.**
We compared both versions of qsort (with a fixed and random pivot) with both ssort and timsort. As expected, ssort was the slowest of them all and as n increases, it became exponentially slower than the qsorts. The runtimes of each are similar to their bounds which further supports our data. Random pivot quicksort was also faster than fixed pivot quicksort, showing that its asymptotic runtime is faster.

Sorted
|      n |   qsort-fixed-pivot |   qsort-random-pivot |   tim-sort |
|--------|---------------------|----------------------|------------|
|    100 |               0.002 |                0.069 |      0.049 |
|    200 |               0.001 |                0.004 |      0.004 |
|    500 |               0.001 |                0.006 |      0.014 |
|   1000 |               0.001 |                0.006 |      0.234 |
|   2000 |               0.001 |                0.007 |      0.284 |
|   5000 |               0.002 |                4.720 |      0.122 |
|  10000 |               0.002 |                0.008 |      0.554 |
|  20000 |               0.003 |                0.008 |      0.295 |
|  50000 |               0.005 |                0.014 |      3.118 |
| 100000 |               0.004 |                0.015 |      2.286 |
 




- **1c.**

We compared the tim-sort within Python to our fastest other sorting method from 1b (which was qsort when it had a random pivot opposed to a fixed one). This is because it could adapt easier to get the fastest runtime while sorting without being restrained to a fixed pivot. However, after comparing it with Timsort, it turns out that timsort is even faster because it can recognize ordered pairs in the list that it does not have to reorder (unlike qsort or ssort that reorder each), which reduces the amount of work and decreases the runtime. 