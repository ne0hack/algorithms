# Generate range of integers


## Description
mplement the function `generateRange` which takes three arguments `(start, stop, step)` and returns the range of integers from `start` to `stop`(inclusive) in increments of `step`.

### Examples

```
(1, 10, 1) -> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
(-10, 1, 1) -> [-10, -9, -8, -7, -6, -5, -4, -3, -2, -1, 0, 1]
(1, 15, 20) -> [1]

```

### Note

-   start < stop
-   step > 0


## Sample Tests
```python
import codewars_test as test
from solution import generate_range

@test.describe("Sample tests")
def test_group():
    @test.it("Simple case")
    def test_case1():
        test.assert_equals(generate_range(1, 10, 1), [1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
    @test.it('Negative numbers')
    def test_case2():
        test.assert_equals(generate_range(-10, 1, 1), [-10, -9, -8, -7, -6, -5, -4, -3, -2, -1, 0, 1])
    @test.it('Step > max')
    def test_case3():
        test.assert_equals(generate_range(1, 15, 20), [1])
    @test.it('Step = 2')
    def test_case4():
        test.assert_equals(generate_range(1, 7, 2), [1, 3, 5, 7])
    @test.it('Step = 3')
    def test_case5():
        test.assert_equals(generate_range(0, 20, 3), [0, 3, 6, 9, 12, 15, 18])
```


## Solution
```python
def generate_range(start, stop, step):
    return list(range(start, stop+1, step))
```
