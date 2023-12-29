# Twice as old


## Description
Your function takes two arguments:

1. current father's age (years)
2. current age of his son (years)

Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old). The answer is always greater or equal to 0, no matter if it was in the past or it is in the future.


## Sample Tests
```python
import codewars_test as test
from solution import twice_as_old

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(twice_as_old(36,7) , 22)
        test.assert_equals(twice_as_old(55,30) , 5)
        test.assert_equals(twice_as_old(42,21) , 0)
        test.assert_equals(twice_as_old(22,1) , 20)
        test.assert_equals(twice_as_old(29,0) , 29)
```


## Solution
### Python
```python
def twice_as_old(dad_years_old, son_years_old):
    if dad_years_old < son_years_old * 2:
        z = 1
    else:
        z = -1
    result = 0
    while dad_years_old != son_years_old * 2:
        dad_years_old += z
        result += 1
    return result
```
