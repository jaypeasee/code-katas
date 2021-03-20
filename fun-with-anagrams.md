# Fun With Anagrams

## Details:
This was a take-home code challenge on HackerRank that I received for a job interview.

## The Brief:
Create a function that takes in an array of strings and returns an array of strings where the consecutive anagrams are removed. 

For example:
`['code', 'doce', 'ecod', 'framer', 'frame'] => [ 'code', 'framer', 'frame' ]`

## My Solution:
```javascript
const funWithAnagrams = (words) => {
  let updatedWords = [words[0]]
  for (let i = 1; i < words.length; i++) {
    if (updatedWords[updatedWords.length -1].split('').sort().join('') !==
        words[i].split('').sort().join('')) {
      updatedWords.push(words[i])
    }
  }
    return updatedWords
}
```

