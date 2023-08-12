# Diagonal Difference


## Description
Given a square matrix, calculate the absolute difference between the sums of its diagonals.\
For example, the square matrix _arr_ is shown below:
```
1 2 3
4 5 6
9 8 9
```
The left-to-right diagonal = _1 + 5 + 9 = 15_. The right to left diagonal = _3 + 5 + 9 = 17_. Their absolute difference is _|15 - 17| = 2_.

**Function description**

Complete the _diagonalDifference_ function in the editor below.\
diagonalDifference takes the following parameter:
- int arr[n][m]: an array of integers

**Return**

- int: the absolute diagonal difference

**Input Format**

The first line contains a single integer, _n_, the number of rows and columns in the square matrix _arr_.\
Each of the next _n_ lines describes a row, _arr[i]_, and consists of _n_ space-separated integers _arr[i][j]_.

**Constraints**

_-100 <= arr[i][j] <= 100_

**Output Format**

Return the absolute difference between the sums of the matrix's two diagonals as a single integer.

**Sample Input**

```
3
11 2 4
4 5 6
10 8 -12
```

**Sample Output**

```
15
```

**Explanation**

The primary diagonal is:
```
11
   5
     -12
```
Sum across the primary diagonal: 11 + 5 - 12 = 4

The secondary diagonal is:
```
     4
   5
10
```
Sum across the secondary diagonal: 4 + 5 + 10 = 19\
Difference: |4 - 19| = 15

**Note:** |x| is the absolute value of x


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
# Complete the 'diagonalDifference' function below.
#
# The function is expected to return an INTEGER.
# The function accepts 2D_INTEGER_ARRAY arr as parameter.
#

def diagonalDifference(arr):
    d1 = 0
    d2 = 0
    z = len(arr[0])-1
    for x in range(len(arr)):
        d1 += arr[x][x]
        d2 += arr[x][z]
        z -= 1
    return abs(d1-d2)

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())

    arr = []

    for _ in range(n):
        arr.append(list(map(int, input().rstrip().split())))

    result = diagonalDifference(arr)

    fptr.write(str(result) + '\n')

    fptr.close()
```

