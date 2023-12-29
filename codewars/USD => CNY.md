# USD => CNY


## Description
Create a function that converts US dollars (USD) to Chinese Yuan (CNY) . The input is the amount of USD as an integer, and the output should be a string that states the amount of Yuan followed by 'Chinese Yuan'

### Examples (Input -> Output)

```
15  -> '101.25 Chinese Yuan'
465 -> '3138.75 Chinese Yuan'

```

The conversion rate you should use is 6.75 CNY for every 1 USD. All numbers should be represented as a string with 2 decimal places. (e.g. "21.00" NOT "21.0" or "21")


## Sample Tests
```python
import codewars_test as test
from solution import usdcny

@test.describe("USD=>CNY")
def test_group():
    @test.it("Basic test case")
    def test_case():
        test.assert_equals(usdcny(15), "101.25 Chinese Yuan")
        test.assert_equals(usdcny(465), "3138.75 Chinese Yuan")
```


## Solution
### Python3
```python
def usdcny(usd):
    res = round(usd * 6.75, 2)
    if len(str(res).split('.')[-1]) == 1:
        return f"{res}0 Chinese Yuan"
    return f"{res} Chinese Yuan"
```
