# Loose Change

## Details:
* <b>Level:</b> 7
* [Code Wars Kata](https://www.codewars.com/kata/5571f712ddf00b54420000ee)

## The Brief:
Create a function that takes an amount of US currency in cents, and returns a dictionary/hash which shows the least amount of coins used to make up that amount. The only coin denominations considered in this exercise are: Pennies (1¢), Nickels (5¢), Dimes (10¢) and Quarters (25¢). Therefor the dictionary returned should contain exactly 4 key/value pairs.

<b>Notes:</b>

If the function is passed either 0 or a negative number, the function should return the dictionary with all values equal to 0.
If a float is passed into the function, its value should be be rounded down, and the resulting dictionary should never contain fractions of a coin.

## My Solution:
```javascript
function looseChange(cents, change = {Quarters: 0, Dimes: 0, Nickels: 0, Pennies: 0}) {
  cents = Math.floor(cents)
  if (!cents) {
    return change
  } else if (cents >= 25) {
    cents -= 25
    change["Quarters"] += 1
    return looseChange(cents, change)
  } else if (cents >= 10) {
    cents -= 10
    change["Dimes"] += 1
    return looseChange(cents, change)
  } else if (cents >= 5) {
    cents -= 5
    change["Nickels"] += 1
    return looseChange(cents, change)
  } else if (cents >= 1) {
    cents -= 1
    change["Pennies"] += 1
    return looseChange(cents, change)
  }
}

looseChange(56)

```



