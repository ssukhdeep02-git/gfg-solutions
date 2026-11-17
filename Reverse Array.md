## 01. Reverse Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-an-array/1)

### Problem Description

**Task:** Given an array of integers arr[], reverse the array in place.Examples:Input: arr = [1, 4, 3, 2, 6, 5]

#### Examples

##### Example 1

- **Output:**
```text
[1]Explanation: The array has only single element, hence the reversed array is same as the original.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-11-17 10:03:52
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    void reverseArray(vector<int> &arr) {
        // code here
        int left = 0;
        int right = arr.size()-1;
        
        while(left<right)
        {
            int temp = arr[left];
            arr[left] = arr[right];
            arr[right] = temp;
            left++;
            right--;
        }
        
    }
};
```

*Generated on: 11/17/2026, 10:05:12 AM*