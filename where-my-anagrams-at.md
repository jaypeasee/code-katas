# Where My Anagrams At?

## The Brief:
Two words are anagrams of each other if they both contain the same letters. Write a function that will find all the anagrams of a word from a list. You will be given two inputs a word and an array with words. You should return an array of all the anagrams or an empty array if there are none.

## My Solution:
```javascript
const anagrams = (word, words) => {
  return words.filter(wordToEval => {
    return alphabetizeString(wordToEval) === alphabetizeString(word)
  })
}

const alphabetizeString = (wordToSort) => {
    return wordToSort.split('').sort().join('')
}

anagrams('racer', ['crazer', 'carer', 'racar', 'caers', 'racer'])
```

