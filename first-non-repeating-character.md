# First Non-Repeating Character

## Details:
* <b>Level</b>: 5
* [Code Wars Kata](https://www.codewars.com/kata/52bc74d4ac05d0945d00054e)

## The Brief:
Write a function that takes a string input, and returns the first character that is not repeated anywhere in the string.

For example, if given the input 'stress', the function should return 't', since the letter t only occurs once in the string, and occurs first in the string.

As an added challenge, upper- and lowercase letters are considered the same character, but the function should return the correct case for the initial letter. For example, the input 'sTreSS' should return 'T'.

If a string contains all repeating characters, it should return an empty string ("")

## My Solution:
```javascript
const firstNonRepeatingLetter = (string) => {
  const totalOccurrances = string.split('').reduce((totals, char) => {
    const upperCase = char.toUpperCase()
    const lowerCase = char.toLowerCase()
    if (!totals[lowerCase] && !totals[upperCase]) {
      totals[char] = 1
    } else {
      totals[upperCase] ? totals[upperCase] += 1 : totals[lowerCase] += 1
    }
    return totals
  }, {})
  
  const uniqueCharacter = Object.keys(totalOccurrances).find(letter => {
    return totalOccurrances[letter] === 1
  })
  
  return uniqueCharacter ? uniqueCharacter : ""
}

firstNonRepeatingLetter('Stress')
```

