# Where My Anagrams At?

## Details:
* <b>Level:</b> 5
* [Code Wars Kata](https://www.codewars.com/kata/523a86aa4230ebb5420001e1)

## The Brief:
Two words are anagrams of each other if they both contain the same letters. Write a function that will find all the anagrams of a word from a list. You will be given two inputs a word and an array with words. You should return an array of all the anagrams or an empty array if there are none.

## My Solution:
```javascript
const findAnagrams = (wordToCompare, possibleAnagrams) => {
  return possibleAnagrams.filter(word => {
    return alphabetizeString(word) === alphabetizeString(wordToCompare)
  })
}

const alphabetizeString = (word) => {
    return word.split('').sort().join('')
}

findAnagrams('racer', ['crazer', 'carer', 'racar', 'caers', 'racer'])
```

