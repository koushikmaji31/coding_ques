Here’s the coding problem written in markdown format:

---

## Problem: Modified Binary Search

You are given a modified binary search algorithm as follows:

```cpp
binarySearch(int l, int r, int s) {
    bool flg = false;
    while(l < r) {
        int mid = (l + r) >> 2;
        if (mid < s) 
            l = mid + 1;
        else if (mid > s) 
            r = mid - 1;
        else {
            flg = true;
            break;
        }
    }
    if (flg != true) 
        cout << "NOT found" << endl;
}
```

Given an interval `[l, r]`, determine the probability that if you choose an integer `i` from this interval, the result of the search for `i` will be "NOT found." Express the probability in the form of `p/q (mod modval)` where `1/q` is the multiplicative inverse of `q` modulo `modval`.

### Input:
- The first line contains an integer `t`, the number of test cases.
- Each of the next `t` lines contains two integers, `l` and `r`, representing the interval.

### Output:
- For each test case, output the probability that the search for a randomly chosen integer `i` from the interval `[l, r]` results in "NOT found."
- The probability should be expressed as `p/q (mod modval)`.

### Constraints:
- `t < 1e7`
- `1 <= l <= r < 1e5`

### Example:
**Input:**
```
2
1 10
3 8
```

**Output:**
```
p/q (mod modval)
p/q (mod modval)
```

---

### Note:
The output should represent the probability that a search in the interval `[l, r]` does not find the value `i`. Use modular arithmetic and multiplicative inverse as required.