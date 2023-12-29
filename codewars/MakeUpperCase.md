# MakeUpperCase


## Description
Write a function which converts the input string to uppercase.


## Sample Tests
```python
import codewars_test as test
from solution import make_upper_case

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(make_upper_case("hello"), "HELLO")
```


## Solution
### Python3
```python
def make_upper_case(s):
    # Code here
    return s.upper()
```
