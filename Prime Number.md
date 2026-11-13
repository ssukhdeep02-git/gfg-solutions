## 01. Prime Number

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/prime-number2314/1)

### Problem Description

**Task:** Given a number n, determine whether it is a prime number or not.Note: A prime number is a number greater than 1 that has no positive divisors other than 1 and itself.Examples :Input: n = 7

#### Examples

##### Example 1

- **Output:**
```text
false
```
- **Explanation:** 1 has only one divisor (1 itself), which is not sufficient for it to be considered prime.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(sqrt(n))
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (C++)

- **Submitted:** 2026-11-13 13:50:13
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    bool isPrime(int n) {
        // code here
        int cnt = 0;
        
        for(int i=1; i*i<=n; i++)
        {
            if(n%i == 0)
            {
                cnt++;
        
                if(n/i != i)
                cnt++;
            }
        }
        
        return cnt == 2;
    }
};
```

#### Solution 2 (C++)

- **Submitted:** 2026-05-17 23:16:13
- **Status:** Correct
- **Marks:** 0

```cpp
class Solution {
  public:
    bool isPrime(int n) {
        int cnt = 0;
        for(int i=1; i*i<=n; i++)
        {
            if(n%i == 0)
            {
                cnt++;
                if(n/i != i)
                cnt++;
            }
        }
        
        return cnt == 2;
    }
};
```

#### Solution 3 (C++)

- **Submitted:** 2026-05-17 23:14:15
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    bool isPrime(int n) {
        int cnt = 0;
        for(int i=1; i<=n; i++)
        {
            if(n%i == 0)
            cnt++;
        }
        
        return cnt == 2;
    }
};
```

*Generated on: 11/13/2026, 1:51:04 PM*