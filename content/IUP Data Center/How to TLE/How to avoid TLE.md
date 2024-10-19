---
title: How to avoid TLE?
draft: false
tags:
  - TLX_Toki
---
### How to avoid TLE?

1. **Optimize the algorithm**:
    
    - Use **binary search** or **dynamic programming** when applicable.
    - Replace O(n2)O(n^2)O(n2) algorithms with more efficient ones (like O(nlog⁡n)O(n \log n)O(nlogn)).
2. **Use fast I/O**:
    
    - For example, in C++, use `scanf`/`printf` instead of `cin`/`cout`, or add:
        
        `ios::sync_with_stdio(false); cin.tie(0);`
		
        
    - In Python, use `sys.stdin.read()` instead of `input()` for large inputs.
1. **Break early**:
    
    - Use **early exits** or **pruning** conditions to stop unnecessary computations.
4. **Use memoization**:
    
    - If you're recalculating results multiple times, store the results and reuse them (as in dynamic programming).
5. **Test edge cases**:
    
    - Before submitting, test your solution with large inputs to verify if it runs within the time limit.