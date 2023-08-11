# Jungerstein's Math Training Room: 1. How many zeros are at the end of n!! ?


## Description
Define n!! as

n!! = 1 * 3 * 5 * ... * n if n is odd, 

n!! = 2 * 4 * 6 * ... * n if n is even. 

Hence 8!! = 2 * 4 * 6 * 8 = 384, there is no zero at the end. 30!! has 3 zeros at the end. 

For a positive integer n, please count how many zeros are there at the end of n!!. 

Example: 

```
30!! = 2 * 4 * 6 * 8 * 10 * ... * 22 * 24 * 26 * 28 * 30
30!! = 42849873690624000 (3 zeros at the end)
```


## Sample Tests
```python
import codewars_test as test
from solution import count_zeros_n_double_fact

@test.describe("Basic tests")
def test_group():
    @test.it("Please pass examples in kata description")
    def test_case():
        test.assert_equals(count_zeros_n_double_fact(8), 0)
        test.assert_equals(count_zeros_n_double_fact(30), 3)
        test.assert_equals(count_zeros_n_double_fact(186), 21)
```


## Solution
### Python3
```python
def count_zeros_n_double_fact(n): 
    num = 1
    for i in range(1 if n % 2 != 0 else 2, n+1, 2):
        num *= i
    result = 0
    for i in str(num)[::-1]:
        if i != "0":
            break
        result += 1
    return result
```
