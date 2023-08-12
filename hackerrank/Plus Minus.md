# Plus Minus


## Description
Given an array of integers, calculate the ratios of its elements that are positive, negative, and zero. Print the decimal value of each fraction on a new line with _6_ places after the decimal.\
**Note:** This challenge introduces precision problems. The test cases are scaled to six decimal places, though answers with absolute error of up to _10**-4_ are acceptable.

**Example**

_arr = [1,1,0,-1,-1]_
There are _n = 5_ elements, two positive, two negative and one zero. Their ratios are _2/5 = 0.4_, _2/5 = 0.4_ and _1/5 = 0.2_. Results are printed as:

**Function Description**

Complete the plusMinus function in the editor below.\
plusMinus has the following parameter(s):
- int arr[n]: an array of integers

**Print**

Print the ratios of positive, negative and zero values in the array. Each value should be printed on a separate line with _6_ digits after the decimal. The function should not return a value.

**Input Format**

The first line contains an integer, _n_, the size of the array.\
The second line contains _n_ space-separated integers that describe _arr[n]._

**Constraints**

_0 < n <= 100_\
_-100 <= arr[i] <= 100_

**Output Format**

**Print** the following _3_ lines, each to _6_ decimals:
1. proportion of positive values
2. proportion of negative values
3. proportion of zeros

**Sample Input**
```
STDIN           Function
-----           --------
6               arr[] size n = 6
-4 3 -9 0 4 1   arr = [-4, 3, -9, 0, 4, 1]
```

**Sample Output**
```
0.500000
0.333333
0.166667
```


## Solution
**Python3**

```python
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'plusMinus' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def plusMinus(arr):
    positive = 0
    negative = 0
    zeros = 0
    for elem in arr:
        if elem == 0:
            zeros += 1
        elif elem < 0:
            negative += 1
        else:
            positive += 1
    positive /= len(arr)
    negative /= len(arr)
    zeros /= len(arr)
    print(positive)
    print(negative)
    print(zeros)

if __name__ == '__main__':
    n = int(input().strip())

    arr = list(map(int, input().rstrip().split()))

    plusMinus(arr)
```
