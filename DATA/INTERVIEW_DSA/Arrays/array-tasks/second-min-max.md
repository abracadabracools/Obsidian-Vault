
### Arrays – 2: Find Second Minimum and Second Maximum in an Array

---

### 1. Problem Statement

Given an array of integers, find the **second smallest** and **second largest** elements.

---

### 2. Algorithm Idea

- **Step 0: How many variables are needed?**
    
    - We need **4 variables**:
        
        - `min_var` → to store the minimum
            
        - `second_min_var` → to store the second minimum
            
        - `max_var` → to store the maximum
            
        - `second_max_var` → to store the second maximum
            
- **Initialize all with null/default:**
    
    - `min_var = +∞`
        
    - `second_min_var = +∞`
        
    - `max_var = -∞`
        
    - `second_max_var = -∞`
        
- **Assign roles and reason:**
    
    - `min_var` and `max_var` will track the extreme values.
        
    - `second_min_var` and `second_max_var` will update whenever we find a new smallest or largest.
        
- **Main Process:**  
    Traverse the array once:
    
    - For minimum:
        
        - If element < `min_var`:
            
            - `second_min_var = min_var`
                
            - `min_var = element`
                
        - Else if element < `second_min_var` and element != `min_var`:
            
            - `second_min_var = element`
                
    - For maximum:
        
        - If element > `max_var`:
            
            - `second_max_var = max_var`
                
            - `max_var = element`
                
        - Else if element > `second_max_var` and element != `max_var`:
            
            - `second_max_var = element`
                
- **End condition:**
    
    - `second_min_var` and `second_max_var` now hold the second smallest and second largest values.
        

---

### 3. Pseudocode

```python
min_var = None
second_min_var = None
max_var = None
second_max_var = None

for element in arr:
    # Minimum tracking
    if min_var is None or element < min_var:
        second_min_var = min_var
        min_var = element
    elif (second_min_var is None or element < second_min_var) and element != min_var:
        second_min_var = element

    # Maximum tracking
    if max_var is None or element > max_var:
        second_max_var = max_var
        max_var = element
    elif (second_max_var is None or element > second_max_var) and element != max_var:
        second_max_var = element

return second_min_var, second_max_var
 ```



---

### 4. Interview Points

- 🕐 Time Complexity: **O(n)**
    
- 💾 Space Complexity: **O(1)**
    
- ⚠️ Edge cases:
    
    - Array length < 2 → no second min/max possible.
        
    - All elements equal → second min/max doesn’t exist.
        
- ✅ Good follow-up to basic min/max.
    
- 💡 Variation: Find **k-th smallest/largest** (can use sorting or heap).