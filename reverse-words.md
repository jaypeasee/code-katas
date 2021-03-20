# Reverse Words

## Details:
* <b>Level:</b> 7
* [Code Wars Kata](https://www.codewars.com/kata/5259b20d6021e9e14c0010d4/javascript)

## The Brief:
Create a function that accepts a string parameter, and reverses each word in the string. All spaces in the string should be retained.

## Examples:
```
"This is an example!" ==> "sihT si na !elpmaxe"
"double  spaces"      ==> "elbuod  secaps"
```

## My Solution:
```javascript
const reverseWords = (str) => {
  return str.split(' ').map(word => {
    return word.split('').reverse().join('')
  }).join(' ')
}

reverseWords('The quick brown fox jumps over the lazy dog.')
```



