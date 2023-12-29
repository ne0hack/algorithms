# Draw stairs


## Description
Given a number `n`, draw stairs using the letter `"I"`, `n` tall and `n` wide, with the tallest in the top left.

For example `n = 3` result in:

```
"I\n I\n  I"

```

or printed:

```
I
 I
  I

```

Another example, a 7-step stairs should be drawn like this:

```
I
 I
  I
   I
    I
     I
      I
```


## Sample Tests
```python
import codewars_test as test
from solution import draw_stairs


@test.describe("Basic Tests")
def basic_tests():
    
    @test.it("Basic Tests")
    def basic_tests():
        test.assert_equals(draw_stairs(3), '''I\n I\n  I''')
        test.assert_equals(draw_stairs(5), '''I\n I\n  I\n   I\n    I''')
```


## Solution
### Python3
```python
def draw_stairs(n):
    result = ''
    for i in range(n):
        result += ' ' * i + 'I\n'
    return result[:-1]
```
