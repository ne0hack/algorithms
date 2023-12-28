# Generate user links


## Description
Your task is to create userlinks for the url, you will be given a username and must return a valid link.

### Example

```
generate_link('matt c')
http://www.codewars.com/users/matt%20c

```

### reference

use this as a reference [encoding](http://www.w3schools.com/tags/ref_urlencode.asp)


## Sample Tests
```python
import codewars_test as test
from solution import generate_link

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        def gen_test_case(inp, res):
            test.assert_equals(generate_link(inp), res, inp)
        gen_test_case('matt c', 'http://www.codewars.com/users/matt%20c')
        gen_test_case('g964', 'http://www.codewars.com/users/g964')
        gen_test_case('GiacomoSorbi', 'http://www.codewars.com/users/GiacomoSorbi')
        gen_test_case('ZozoFouchtra', 'http://www.codewars.com/users/ZozoFouchtra')
        gen_test_case('colbydauph', 'http://www.codewars.com/users/colbydauph')
```


## Solution
```python
from urllib.parse import quote

def generate_link(user):
    return 'http://www.codewars.com/users/' + quote(user.encode('utf-8'))
```

