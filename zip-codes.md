# Zip Codes

## The Brief:
Given a string, check to see if the value is a valid ZIP code. Valid ZIP codes are strings with five number characters.

## My Solution 

```javascript
const checkZip = (input) => {
  return parseInt(input).toString().length === 5 ? true : false
}

checkZip('1er44')
```

