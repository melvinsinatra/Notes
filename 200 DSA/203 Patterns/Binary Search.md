- Ensure the input data structure (usually an array) is **sorted**.
- Define two pointers:
    - `left` → start index (usually `0`)
    - `right` → end index (`array.length - 1`)
- Repeat while `left <= right`:
    - Compute the middle index:  
        `mid = Math.floor((left + right) / 2)`
    - Compare the middle element with the target value:
        - If `array[mid] === target`, return `mid` (found).
        - If `array[mid] < target`, move the search right:  
            `left = mid + 1`
        - If `array[mid] > target`, move the search left:  
            `right = mid - 1`
- If the loop ends without finding the target, return a sentinel value (commonly `-1`).
- Time complexity: **O(log n)**
- Space complexity:
    - **O(1)** for iterative implementation
    - **O(log n)** for recursive implementation (due to call stack)