# [Longest-vowel-chain](https://www.codewars.com/kata/59c5f4e9d751df43cf000035)

This function finds the length of a longest vowel substring (several vowels standing together) inside a given word. 

## Syntax

> solve(`string`) -> `number`

### Parameters

**s**: `string`

- The given word inside which the longest vowel substring will be searched.

### Return Value: `number`

The length of the longest vowel substring.

## Examples


description:

```js
const max = solve("codewarriors");
console.log(max)// 2
```

```js
const max = solve("cuboideonavicuare");
console.log(max)// 2
```

```js
const max = solve("iiihoovaeaaaoougjyaw");
console.log(max)// 8
---



## [ooflorent](https://www.codewars.com/users/ooflorent)

```js
function solve(s) {
  let cur = 0
  let max = 0
  for (let i = 0; i < s.length; ++i) {
    if ("aeiou".includes(s[i])) {
      cur++
      if (cur > max) {
        max = cur
      }
    } else {
      cur = 0
    }
  }
  return max
}
```

### Strategy

The function iterates through the given string and finds the length of the longest string of subsequent vowels. 

### Implementation

Two variable are defined, one of which counts the length of the current string of vowels and the other keeping the count of the maximum to the present point. A for loop iterates through the characters in the string, checks for vowels in each iteration. Increments the current variable for each vowel and max variable as long as the value of current is higher than max. In case the iterator meets a consonant it resets the current value but leaves max untouched, therefore max value is kept intact.


**for loop**: iterates through the characters in the string, checks for vowels in each iteration
**if/else statement**: checks if a character is a vowel or not
**includes() method**: checks whether a given string contains the vowels

### Possible Refactors

This strategy could also be implemented with the following methods:

- `while` loop;
- `split` method;
- `reduce` method

---



## [joanna.gargas](https://www.codewars.com/users/joanna.gargas)

```js
function solve(s){
 return Math.max(...s.match(/[aeiou]+/g).map(x => x.length));
}
```

### Strategy

This function extracts the groups of vowels from the given string and returns the length of the longest one.


### Implementation

The string is compared against a regex to find groups of vowels. The array that's returned from the match method is mapped in order to find the lengths of items. Resulting array is spread as the parameters of the math max method in order to find the highest number and return it.

**match method**: returns an array of strings that match the given regex conditions
**map method**: returns an array with the lengths of each elements of the given array
**spread operator**: spreads the values of the array as parameters of math max method
**Math.max method**: returns the highest value among the arguments



### Possible Refactors

This strategy could also be implemented with the following:

- `if else` statement;
- `for`loop;


---

## Notes

I learnt a lot of new methods from second solution of the challenge, like match, math.max, also understood what spread operator is used for.