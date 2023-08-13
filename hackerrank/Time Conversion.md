# Time Conversion


## Description
Given a time in 12-hour AM/PM format, convert it to military (24-hour) time.\
Note: 
- 12:00:00AM on a 12-hour clock is 00:00:00 on a 24-hour clock.
- 12:00:00PM on a 12-hour clock is 12:00:00 on a 24-hour clock.

**Example**

* _12:01:00PM_
Return '12:01:00'.

* _12:01:00AM_
Return '00:01:00'.

**Function Description**

Complete the timeConversion function in the editor below. It should return a new string representing the input time in 24 hour format.\
timeConversion has the following parameter(s):
- string s: a time in _12_ hour format

**Returns**

- string: the time in _24_ hour format

**Input Format**

A single string _s_ that represents a time in 12-hour clock format (i.e.: _hh:mm:ssAM_ or _hh:mm:ssPM_).

**Constraints**

- All input times are valid

**Sample Input 0**

```
07:05:45PM
```

**Sample Output 0**

```
19:05:45
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
# Complete the 'timeConversion' function below.
#
# The function is expected to return a STRING.
# The function accepts STRING s as parameter.
#

def timeConversion(s):
    mapping_time = {
        "01": "13", 
        "02": "14", 
        "03": "15", 
        "04": "16",
        "05": "17", 
        "06": "18",
        "07": "19",
        "08": "20",
        "09": "21",
        "10": "22",
        "11": "23"
    }
    if "PM" in s:
        s = s[:-2].split(":")
        s[0] = mapping_time.get(s[0], s[0])
        return ":".join(s)
    else:
        s = s[:-2].split(":")
        if s[0] == "12":
            s[0] = "00"
        return ":".join(s)

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    s = input()

    result = timeConversion(s)

    fptr.write(result + '\n')

    fptr.close()
```
