# Not very secure


## Description
In this example you have to validate if a user input string is alphanumeric. The given string is not `nil/null/NULL/None`, so you don't have to check that.

The string has the following conditions to be alphanumeric:

-   At least one character (`""` is not valid)
-   Allowed characters are uppercase / lowercase latin letters and digits from `0` to `9`
-   No whitespaces / underscore


## Sample Tests
```python
@test.describe("Sample Tests")
def sample_tests():
    tests = [
        ("hello world_", False),
        ("PassW0rd", True),
        ("     ", False)
    ]
    for s, b in tests:
        @test.it('alphanumeric("' + s + '")')
        def sample_test():
            test.assert_equals(alphanumeric(s), b)
```


## Solution
```python
def alphanumeric(password):
    was_alpha = False
    for i in password:
        if i.isalpha():
            was_alpha = True
        elif not i.isdigit():
            return False
    if not was_alpha:
        return False
    return True
```
