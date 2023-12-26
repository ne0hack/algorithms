# Exclamation marks series #1: Remove an exclamation mark from the end of string


## Description
Remove an exclamation mark from the end of a string. For a beginner kata, you can assume that the input data is always a string, no need to verify it.

### Examples

```
"Hi!"     ---> "Hi"
"Hi!!!"   ---> "Hi!!"
"!Hi"     ---> "!Hi"
"!Hi!"    ---> "!Hi"
"Hi! Hi!" ---> "Hi! Hi"
"Hi"      ---> "Hi"
```


## Sample Tests
```python
import codewars_test as test
from solution import remove

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():

        tests = [
            #[input, [expected]],
            ["Hi!", "Hi"],
            ["Hi!!!","Hi!!"],
            ["!Hi", "!Hi"],
            ["!Hi!", "!Hi"],
            ["Hi! Hi!", "Hi! Hi"],
            ["Hi", "Hi"],
            ["", ""],
        ]

        for inp, exp in tests:
            test.assert_equals(remove(inp), exp)
```


## Solution
### Python3
```python
def remove(s):
    if s and s[-1] == '!':
        return s[:-1]
    return s
```
