# easy logs


## Description
Add two logs with base X, with the value of A and B. Example log A + log B where the base is X.


## Sample Tests
```python
import codewars_test as test
from solution import logs

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_approx_equals(logs(10, 2, 3), 0.7781512503836435)
        test.assert_approx_equals(logs(5, 2, 3), 1.1132827525593785)
        test.assert_approx_equals(logs(1000, 2, 3), 0.25938375012788123)
        test.assert_approx_equals(logs(2, 1, 2), 1)
        test.assert_approx_equals(logs(0.00001, 0.002, 0.01), 0.9397940008672038)
        test.assert_approx_equals(logs(0.1, 0.002, 0.01), 4.69897000433602)
```


## Solution
```python
from math import log

def logs(x, a, b):
    return log(a*b, x)
```
