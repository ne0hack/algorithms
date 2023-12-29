# Get Planet Name By ID


## Description
The function is not returning the correct values. Can you figure out why?

Example (**Input** --> **Output** ):

```
3 --> "Earth"
```


## Sample Tests
```python
import codewars_test as test
from solution import get_planet_name

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(get_planet_name(2), 'Venus')
        test.assert_equals(get_planet_name(5), 'Jupiter')
        test.assert_equals(get_planet_name(3), 'Earth')
        test.assert_equals(get_planet_name(4), 'Mars')
        test.assert_equals(get_planet_name(8), 'Neptune')
        test.assert_equals(get_planet_name(1), 'Mercury')
```


## Solution
### Python
```python
def get_planet_name(id):
    mapping = {
        1: "Mercury",
        2: "Venus",
        3: "Earth",
        4: "Mars",
        5: "Jupiter",
        6: "Saturn",
        7: "Uranus",  
        8: "Neptune",
    }
    return mapping[id]
```
