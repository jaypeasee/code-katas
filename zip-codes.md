# Zip Codes

## Details:
This is a common screen interview problem at my company.

## The Brief:
Given a string, check to see if the value is a valid ZIP code. Valid ZIP codes are strings with five number characters.

## My Solution 

```javascript
const checkZip = (input) => {
  const legalNums = ["0", "1", "2", "3", "4", "5", "6", "7", "8", "9"]
  for (let i = 0; i < input.length; i++) {
    if (!legalNums.includes(input[i]) || input.length !== 5) {
      return false
    }
  }
  return true
}

checkZip("11245TT")
```
