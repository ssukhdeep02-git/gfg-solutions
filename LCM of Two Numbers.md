## 01. LCM of Two Numbers

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/lcm-of-two-numbers/1)

### Problem Description

**Task:** Given two positive integers a and b, find the Least Common Multiple (LCM) of the two numbers.Examples:Input: a = 12, b = 18Output: 36Explanation: LCM of 12 and 18 is 36Input: a = 5, b = 11Output: 55Explanation: LCM of 5 and 11 is 55

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log(min(a,b))
- **Expected Auxiliary Space Complexity:** O(log(min(a,b))

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-11-13 15:09:47
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    int lcm(int a, int b) {
        // code here
        int n1 = a, n2 = b;
        while(a>0 && b>0)
        {
            if(a>b) a %= b;
            else
            b%=a;
        }
        
        int gcd;
        
        if(a==0) gcd = b;
        else gcd = a;
    
        int lcm = (n1*n2)/gcd;
        
        return lcm;
    }
};
```

*Generated on: 11/13/2026, 3:10:35 PM*