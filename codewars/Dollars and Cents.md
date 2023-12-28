# Dollars and Cents


## Description
The company you work for has just been awarded a contract to build a payment gateway. In order to help move things along, you have volunteered to create a function that will take a float and return the amount formatting in dollars and cents.

`39.99 becomes $39.99`

The rest of your team will make sure that the argument is sanitized before being passed to your function although you will need to account for adding trailing zeros if they are missing (though you won't have to worry about a dangling period).

Examples:

```
3 needs to become $3.00

3.1 needs to become $3.10
```


## Sample Tests
```python
import codewars_test as test
from solution import format_money

@test.describe("Fixed Tests")
def fixed_tests():
    @test.it('Basic Test Cases')
    def basic_test_cases():
        test.assert_equals(format_money(0), '$0.00')
        test.assert_equals(format_money(39.9), '$39.99')
        test.assert_equals(format_money(81), '$81.00')
```


## Solution
```python
def format_money(amount):
    if type(amount) == int:
        return f'${amount}.00'
    elif len(str(amount).split('.')[-1]) == 1:
        return f'${amount}0'
    return f'${amount}'
```
