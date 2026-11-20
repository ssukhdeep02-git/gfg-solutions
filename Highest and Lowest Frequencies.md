## 01. Highest and Lowest Frequencies

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/difference-between-highest-and-lowest-occurrence4613/1)

### Problem Description

**Task:** Given an array, the task is to find the difference between the highest occurrence and lowest occurrence of any numbers in an array. If only one type of element is present in the array return 0Examples:Input: arr[] = [1, 2, 2]

#### Examples

##### Example 1

- **Output:**
```text
2
```
- **Explanation:** Lowest occurring element (2) occurs once. Highest occurring element (7) occurs 3 times

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-11-20 11:03:48
- **Status:** Correct
- **Marks:** 1

```cpp
class Solution {
  public:
    int findDiff(vector<int>& arr) {
        // code here
        if(arr.empty())
        return -1;
        
        if(arr.size() == 1)
        return 0;
        
        int highestFreq = INT_MIN, highestElement = -1;
        int lowestFreq = INT_MAX, lowestElement = -1;
        
        unordered_map <int,int> freq;
        
        for(auto it : arr)
        {
            freq[it]++; //frequency of the elements stored in the hashmap
        }
        
        for(auto it: freq)
        {
            int currValue = it.first;
            int currFreq = it.second;
            
            if(currFreq > highestFreq)
            {
                highestFreq = currFreq;
                highestElement = currValue;
            }
            
            if(currFreq < lowestFreq)
            {
                lowestFreq = currFreq;
                lowestElement = currValue;
            }
        }
        
        return highestFreq - lowestFreq;
    }
};
```

*Generated on: 11/20/2026, 11:04:19 AM*