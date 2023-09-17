# Failed Filter - Bug Fixing #3


## Description
Oh no, Timmy's filter doesn't seem to be working? Your task is to fix the FilterNumber function to remove all the numbers from the string.


## Sample Tests
```python
import codewars_test as test
from solution import filter_numbers

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(filter_numbers("test123"), 'test', 'Just return the string')
        test.assert_equals(filter_numbers("a1b2c3"), 'abc', 'Just return the string')
        test.assert_equals(filter_numbers("aa1bb2cc3dd"), 'aabbccdd', 'Just return the string')
        test.assert_equals(filter_numbers("CodeWars"), 'CodeWars', 'Just return the string')
        test.assert_equals(filter_numbers("99234"), '', 'Just return the string')
```


## Solution
### Python3
```python
def filter_numbers(string):
    return "".join(x for x in string if not x.isdigit())
```
