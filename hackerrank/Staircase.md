# Staircase


## Description
Staircase detail\
This is a staircase of size _n = 4_:
```
   #
  ##
 ###
####
```
Its base and height are both equal to n. It is drawn using # symbols and spaces. The last line is not preceded by any spaces.\
Write a program that prints a staircase of size n.

**Function Description**

Complete the staircase function in the editor below.
staircase has the following parameters):
- int n: an integer

**Print**

Print a staircase as described above.

**Input Format**

A single integer, n, denoting the size of the staircase.

**Constraints**

0 < n < 100.

**Output Format**

Print a staircase of size n using # svmbols and spaces.\
**Note:** The last line must have _0_ spaces in it.

**Sample Input**

```
6
```

**Sample Output**

```
     #
    ##
   ###
  ####
 #####
######
```

**Explanation**

The staircase is right-aligned, composed of # symbols and spaces, and has a height and width of _n = 6_.


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
# Complete the 'staircase' function below.
#
# The function accepts INTEGER n as parameter.
#

def staircase(n):
    result = ["#" * n]
    for i in range(n-1):
        result.append(result[-1].replace("#", " ", 1))
    print("\n".join(result[::-1]))
    

if __name__ == '__main__':
    n = int(input().strip())

    staircase(n)
```
