## 01. Most Frequent in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/most-frequent-element-in-an-array/1)

### Problem Description

**Task:** You are given an integer array arr[], return the element which occurs maximum times. If multiple such elements exists return the maximum element.Example: Input: arr[] = [1, 2, 2, 2, 4, 1]Output: 2Explanation: 2 is most frequent element of this array with 3 occurrences.Input: arr[] = [1, -5, 8, 1]Output: 1Explanation: 1 is most frequent element of this array with 2 occurrences.Input: arr[] = [3, 0, 0, 3, 8]Output: 3Explanation: 0 and 3 are two most frequent elements of this array. 3 is the maximum one.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-11-20 10:23:45
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    int mostFreqEle(vector<int>& arr) {
        // code here
        if(arr.empty())
        return -1;
        
        int maxFreq = 0;
        int answer = arr[0];
        
        unordered_map <int,int> freq;
        
        for(int value: arr)
        {
            int currFreq = ++freq[value];
            
            if(currFreq > maxFreq || (currFreq == maxFreq && value > answer))
            {
                maxFreq = currFreq;
                answer = value;
            }
        }
        
        return answer;
    }
};
```

*Generated on: 11/20/2026, 10:26:30 AM*