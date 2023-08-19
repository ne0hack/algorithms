# Birthday Cake Candles


## Description
You are in charge of the cake for a child's birthday. You have decided the cake will have one candle for each year of their total age.\
They will only be able to blow out the tallest of the candles. Count how many candles are tallest.

**Example**

candles = [4, 4, 1, 3]\
The maximum height candles are 4 units high. There are 2 of them, so return 2.

**Function Description**

Complete the function birthdayCakeCandles in the editor below.\
birthdayCakeCandles has the following parameters):
- int candles[n]: the candle heights

**Returns**

- int: the number of candles that are tallest

**Input Format**

The first line contains a single integer, n, the size of _candles[]_.\
The second line contains n space-separated integers, where each integer _i_ describes the height of _candles[i]_.

**Constraints**

- 1 < n < 105
- 1 < candles[i] < 10^7

**Sample Input 0**

```
4
3 2 1 3
```

**Sample Output 0**

```
2
```

**Explanation 0**
Candle heights are [3, 2, 1, 3]. The tallest candles are 3 units, and there are 2 of them.


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
# Complete the 'birthdayCakeCandles' function below.
#
# The function is expected to return an INTEGER.
# The function accepts INTEGER_ARRAY candles as parameter.
#

def birthdayCakeCandles(candles):
    return candles.count(max(candles))

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    candles_count = int(input().strip())

    candles = list(map(int, input().rstrip().split()))

    result = birthdayCakeCandles(candles)

    fptr.write(str(result) + '\n')

    fptr.close()
```
