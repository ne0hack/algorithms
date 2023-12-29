# Hello, Name or World!


## Description
Define a method `hello` that `returns` "Hello, Name!" to a given `name`, or says Hello, World! if name is not given (or passed as an empty String).

Assuming that `name` is a `String` and it checks for user typos to return a name with a first capital letter (Xxxx).

Examples:

```
* With `name` = "john"  => return "Hello, John!"
* With `name` = "aliCE" => return "Hello, Alice!"
* With `name` not given
  or `name` = ""        => return "Hello, World!"
```


## Sample Tests
```python
import codewars_test as test
from solution import hello

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        
        tests = (
            ("John", "Hello, John!"),
            ("aLIce", "Hello, Alice!"),
            ("", "Hello, World!"),
        )
        
        for inp, exp in tests:
            test.assert_equals(hello(inp), exp)

        test.assert_equals(hello(), "Hello, World!")
```


## Solution
```python
def hello(name: str = "World"):
    if not name:
        name = "World"
    name = name[0].upper() + name[1:].lower()
    return f"Hello, {name}!"
```
