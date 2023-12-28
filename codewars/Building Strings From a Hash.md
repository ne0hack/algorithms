# Building Strings From a Hash


## Description
Complete the solution so that it takes the object (JavaScript/CoffeeScript) or hash (ruby) passed in and generates a human readable string from its key/value pairs. 

The format should be "KEY = VALUE". Each key/value pair should be separated by a comma except for the last pair.

**Example:**

```
solution({"a": 1, "b": '2'}) # should return "a = 1,b = 2"
```


## Sample Tests
```python
import codewars_test as test
from solution import *

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(solution({'a': 1, 'b': 2}), 'a = 1,b = 2')
        test.assert_equals(solution({'a': 'b', 'b': 'a'}), 'a = b,b = a')
        test.assert_equals(solution({0: 'a', 'b': 2}), '0 = a,b = 2')
        test.assert_equals(solution({'b': 1, 'c': 2, 'e': 3}), 'b = 1,c = 2,e = 3')
        test.assert_equals(solution({}), '')
```


## Solution
```python
def solution(pairs):
    result = ""
    for key, value in pairs.items():
        if result:
            result += ','
        result += f'{key} = {value}'
    return result
```
