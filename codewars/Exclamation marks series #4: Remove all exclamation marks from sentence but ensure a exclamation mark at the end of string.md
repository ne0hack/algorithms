# Exclamation marks series #4: Remove all exclamation marks from sentence but ensure a exclamation mark at the end of string


## Description
Remove all exclamation marks from sentence but ensure a exclamation mark at the end of string. For a beginner kata, you can assume that the input data is always a non empty string, no need to verify it.

### Examples

```
"Hi!"     ---> "Hi!"
"Hi!!!"   ---> "Hi!"
"!Hi"     ---> "Hi!"
"!Hi!"    ---> "Hi!"
"Hi! Hi!" ---> "Hi Hi!"
"Hi"      ---> "Hi!"
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
            ["Hi!" , "Hi!"],
            ["Hi!!!" ,"Hi!"],
            ["!Hi" , "Hi!"],
            ["!Hi!" , "Hi!"],
            ["Hi! Hi!" , "Hi Hi!"],
            ["Hi" , "Hi!"],
        ]

        for inp, exp in tests:
            test.assert_equals(remove(inp), exp)
```


## Solution
### Python
```python
def remove(st):
    return st.replace('!', '') + '!'
```
