# Find the maximum number of hotel visitors


## Description
Given a hotel and dates with amount of arrival visitors and leaving visitors.

date -> amount of visitors (arrival)

date -> amount of visitors (leave)

Write a code that outputs maximim amount of visitors in one day at the hotel.

#### Example 1:
```
Input:
arrival
'1' - 5
'2' - 1
'3' - 6
'4' - 15

leaves
'1' - 0 
'2' - 0
'4' - 6
'5' - 20

Output:
21
```


## Solution

### Python3
```python
class Solution:
    def countMaxVisitors(self, arrivals, leavings):
        # сортируем дни прибытия убытия
        arrivals = sorted(arrivals, key=lambda x: x[0])
        leavings = sorted(leavings, key=lambda x: x[0])
        # результат и временное знач в настоящ время
        result = 0
        temp = 0

        i_arr, i_leav = 0, 0
        while i_arr < len(arrivals):
            # если никто не убывает или день прибытия меньше дня убытия
            if (i_leav >= len(leavings)) or (arrivals[i_arr][0] < leavings[i_leav][0]):
                temp += arrivals[i_arr][1]
                i_arr += 1
            # если только убывают, но еще не наступил день убытия
            elif arrivals[i_arr][0] > leavings[i_leav][0]:
                temp -= leavings[i_leav][1]
                i_leav += 1
            # если сегодня и убывают и прибывают
            else:
                temp += arrivals[i_arr][1] - leavings[i_leav][1]
                i_arr += 1
                i_leav += 1

            result = max(result, temp)

        return result


sol = Solution()

arrivals = [(1, 5), (2, 1), (3, 6), (4, 15)]
leavings = [(1, 0), (2, 0), (4, 6), (5, 20)]
result = 21
assert sol.countMaxVisitors(arrivals, leavings) == result

arrivals = [(1, 10)]
leavings = [(1, 0), (2, 1), (4, 1), (5, 1)]
result = 10
assert sol.countMaxVisitors(arrivals, leavings) == result

arrivals = [(4, 2), (5, 10)]
leavings = [(1, 0), (2, 0), (4, 0), (5, 1)]
result = 11
assert sol.countMaxVisitors(arrivals, leavings) == result

arrivals = []
leavings = [(1, 0), (2, 0), (3, 0)]
result = 0
assert sol.countMaxVisitors(arrivals, leavings) == result   


arrivals = []
leavings = []
result = 0
assert sol.countMaxVisitors(arrivals, leavings) == result 

arrivals = [(4, 2), (5, 10)]
leavings = []
result = 12
assert sol.countMaxVisitors(arrivals, leavings) == result

arrivals = [(4, 2), (5, 10)]
leavings = [(4, 0), (5, 0)]
result = 12
assert sol.countMaxVisitors(arrivals, leavings) == result
```

