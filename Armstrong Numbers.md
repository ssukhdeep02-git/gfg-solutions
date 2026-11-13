## 01. Armstrong Numbers

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/armstrong-numbers2727/1)

### Problem Description

**Task:** Given a positive integer n, determine whether it is an Armstrong number or not.An Armstrong number is a number where, sum of each digit raised to the power digit count, is equal to the original number.Examples:Input: n = 153

#### Examples

##### Example 1

- **Output:**
```text
true
```
- **Explanation:** 1³ + 5³ + 3³ = 153, which is equal to the original number.

##### Example 2

- **Input:**
```text
n = 1634Output: true
```
- **Output:**
```text
false
```
- **Explanation:** 1³ + 0³ + 0³ = 1, which is not equal to 100.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(d), where d is the number of digits in nAuxiliary Space: O(d)
- **Expected Auxiliary Space Complexity:** O(d)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-05-17 23:03:43
- **Status:** Correct
- **Marks:** 2

```cpp
// User function Template for C++
class Solution {
  public:
    bool armstrongNumber(int n) {
        int sum = 0, digit = 0;
        int original = n;
        
        while(n)
        {
            digit = n%10;
            sum += pow(digit,3);
            n = n/10;
        }
        
        return sum == original;
        
    }
};
```

*Generated on: 11/13/2026, 12:57:33 PM*