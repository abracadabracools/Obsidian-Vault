Go back - [[Arrays Glossary]]
# 📆 Day 1 – Arrays – 1: Find Maximum and Minimum Element in an Array

---

### 1. Problem Statement

Given an array of `n` integers, find the maximum and minimum elements in the array.

---

### 2. Algorithm Idea

- **Step 0: How many variables are needed?**
    
    - We need **2 variables** to keep track of the minimum and maximum values.
        
- **Initialize all with null / default:**
    
    - `min_var = +∞` (or `arr[0]` if array is not empty)
        
    - `max_var = -∞` (or `arr[0]` if array is not empty)
        
- **Assign values and reason:**
    
    - Initialize both to the first element because it is the best known min and max so far.
        
    - Then traverse the array and compare each element with `min_var` and `max_var`.
        
- **Main Process:**
    
    - If current element < `min_var` → update `min_var`.
        
    - If current element > `max_var` → update `max_var`.
        
- **End condition:**
    
    - After traversal, `min_var` and `max_var` hold the smallest and largest values.
        

---

### 3. Pseudocode
```
if element > max_var:  
    second_max_var = max_var  
    max_var = element  
elif element > second_max_var and element != max_var:  
    second_max_var = element
``` 
  
---

### 4. Interview Points

- 🕐 Time Complexity: **O(n)**
    
- 💾 Space Complexity: **O(1)**
    
- Edge cases: empty array (handle separately), single-element array.
    
- Optimization: Can reduce comparisons slightly using pairwise checking.
    
- Variants:
    
    - Find second min/max.
        
    - Find min/max in a rotated sorted array.