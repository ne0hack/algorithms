# Multiply the number


## Description
Jack really likes his number five: the trick here is that you have to multiply each number by 5 raised to the number of digits of each numbers, so, for example:

```
multiply(3)==15 # 3 * 5¹
multiply(10)==250 # 10 * 5²
multiply(200)==25000 # 200 * 5³
multiply(0)==0 # 0 * 5¹
multiply(-3)==-15 # -3 * 5¹
```


## Sample Tests
```python
import codewars_test as test
from solution import multiply

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(multiply(10),250)
        test.assert_equals(multiply(5),25)
        test.assert_equals(multiply(200),25000)
        test.assert_equals(multiply(0),0)
        test.assert_equals(multiply(-2),-10)
```


## Solution
### Python3
```python
def multiply(n):
    return n * (5 ** len(str(n).replace('-', '')))
```
