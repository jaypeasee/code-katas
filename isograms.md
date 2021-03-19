# Isograms

## Details:
* <b>Level:</b> 7
* [Code Wars Kata](https://www.codewars.com/kata/54ba84be607a92aa900000f1/javascript)

## The Brief:
An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

## My Solution:
```javascript
const checkIsogram = (str) => {
  let letters = {}
  for (let i = 0; i < str.length; i++) {
    if (!letters[str[i].toLowerCase()]) {
      letters[str[i].toLowerCase()] = 1
    } else {
      return false
    }
  }
  return true
}

checkIsogram("MoOse")
```

