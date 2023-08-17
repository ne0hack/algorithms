# Mini-Max Sum


## Description
Given five positive integers, find the minimum and maximum values that can be calculated by summing exactly four of the five integers. Then print the respective minimum and maximum values as a single line of two space-separated long integers.

**Example**

_arr = [1,3,5,7,9]_

The minimum sum is _1 + 3 + 5 + 7 = 16_ and the maximum sum is _3 + 5 + 7 + 9 = 24_. The function prints
```
16 24
```

**Function Description**

Complete the miniMaxSum function in the editor below.
miniMaxSum has the following parameter(s):
- arr: an array of _5_ integers

**Print**

Print two space-separated integers on one line: the minimum sum and the maximum sum of _4_ of _5_ elements.

**Input Format**

A single line of five space-separated integers.

**Constraints**

_1 <= arr[i] <= 10**9_

**Output Format**

Print two space-separated long integers denoting the respective minimum and maximum values that can be calculated by summing exactly four of the five integers. (The output can be greater than a 32 bit integer.)

**Sample Input**

```
1 2 3 4 5
```

**Sample Output**

```
10 14
```

**Explanation**

The numbers are 1, 2, 3, 4, and 5. Calculate the following sums using four of the five integers:
1. Sum everything except 1, the sum is 2 + 3 + 4 + 5 = 14.
2. Sum everything except 2, the sum is 1 + 3 + 4 + 5 = 13.
3. Sum everything except 3, the sum is 1 + 2 + 4 + 5 = 12.
4. Sum everything except 4, the sum is 1 + 2 + 3 + 5 = 11.
5. Sum everything except 5, the sum is 1 + 2 + 3 + 4 = 10.

**Hints:** Beware of integer overflow! Use 64-bit Integer.


## Solution
**Python 3**

```python
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'miniMaxSum' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def miniMaxSum(arr):
    arr.sort()
    print(sum(arr[:4]), sum(arr[-4:]))

if __name__ == '__main__':

    arr = list(map(int, input().rstrip().split()))

    miniMaxSum(arr)
```


