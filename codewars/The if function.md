# The 'if' function


## Description
Create a function called `_if` which takes 3 arguments: a value `bool` and 2 functions (which do not take any parameters): `func1` and `func2`

When `bool` is truthy, `func1` should be called, otherwise call the `func2`.

### Example:

```python
def truthy():
  print("True")

def falsey():
  print("False")

_if(True, truthy, falsey)
# prints 'True' to the console
```


## Sample Tests
```python
from solution import _if
import codewars_test as test

@test.describe("Sample tests")
def sample_tests():
    @test.it("Tests")
    def it_1():
        a = b = c = d = e = False
        
        def a1():
        	test.expect(True)
        	nonlocal a
        	a = True
        
        def a2():
        	test.expect(False, "Should respond to True correctly")
        
        def b1():
        	test.expect(False, "Should support falsy/truthy values")
        
        def b2():
        	test.expect(True)
        	nonlocal b
        	b = True
        
        def c1():
        	test.expect(True)
        	nonlocal c
        	c = True
        
        def c2():
        	test.expect(False, "Should support falsy/truthy values")
        
        def d1():
        	test.expect(True)
        	nonlocal d
        	d = True
        
        def d2():
        	Test.expect(False, "Should support comparison")
        
        def e1():
        	test.expect(True)
        	nonlocal e
        	e = True
        
        def e2():
        	test.expect(False, "Should support comparison")
        
        _if(True, a1, a2)
        _if(False, b1, b2)
        _if(1, c1, c2)
        _if((3 < 4), d1, d2)
        _if((9 % 3 == 0), e1, e2)
        
        test.expect(a and b and c and d and e)
```


## Solution
### Python3
```python
def _if(bool, func1, func2):
    if bool:
        func1()
    else:
        func2()
```
