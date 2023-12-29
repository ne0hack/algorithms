# Return Negative


## Description
In this simple assignment you are given a number and have to make it negative. But maybe the number is already negative?

### Examples

```
make_negative(1);  # return -1
make_negative(-5); # return -5
make_negative(0);  # return 0

```

### Notes

-   The number can be negative already, in which case no change is required.
-   Zero (0) is not checked for any specific sign. Negative zeros make no mathematical sense.


## Sample Tests
```python
import codewars_test as test
from solution import make_negative

@test.describe("Fixed Tests")
def basic_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        for n, expected in ((42,-42), (-9,-9), (0,0)):
            actual = make_negative(n)
            message = f"For n = {n}, expected {expected} but got {actual}"
            test.assert_equals(actual, expected, message)
```


## Solution
### Python3
```python
def make_negative( number ):
    if number > 0:
        return number * -1
    return number
```
