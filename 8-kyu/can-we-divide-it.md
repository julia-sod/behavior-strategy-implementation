# [Can we divide it?](https://www.codewars.com/kata/5a2b703dc5e2845c0900005a)

With the help of this function you can check if the first given number is divisible by each of two following numbers. The function will return true if it's divisible and false if it's not divisible by at least one of the following numbers.

## Syntax

> isDivideBy(`number`, `number`, `number`) -> `boolean`

### Parameters

**number, a, b**: `number`

- Any 3 integer numbers.

### Return Value: `boolean`

True or false, depending on if a number is divisible or not.

## Examples

This function's behavior is relatively simple to understand. This exercise didn't include complicated edge case.



```js
const a = 2
const b = 1
const number = -14
const result = isDivideBy(number, a, b)
console.log(result) //true


const a = 2
const b = 5
const number = 12
const result = isDivideBy(number, a, b)
console.log(result) //false

```




## [YetiNaga](https://www.codewars.com/kata/reviews/5a2b77018b2221499d000960/groups/5a2d7edd4f89bcf2e9000237)

```js
let isDivideBy = (number, a, b) => {
  if (number % a === 0 && number % b === 0) {
    return true
  } else {
    return false
  }
}
```

### Strategy

This solution is very easy and visual, it shows every step clearly. Function checks if one number can be divided by second and third given numbers.


### Implementation

Yeti used the remainder operator that returns the remainder left over when one operand is divided by a second operand. As it is equal to 0, a number is divisible.


**if/else statement**: checks if the results of both remainder operations are equal to 0.

### Possible Refactors

This strategy could also be implemented with these Implementation ...

- conditional operator `?:`


---


## [altirovskimiki](https://www.codewars.com/kata/reviews/5a2b77018b2221499d000960/groups/5a2c4ac6971dc4bd9f001d80)

```js
function isDivideBy(number, a, b) {
  return (number%a + number%b) === 0
}
```

### Strategy

Function shows if one number can be divided by second and third given numbers by checking their sum.

### Implementation

In this solution a remainder operator is used too but the difference is, that the sum of both results is checked.


**operator precedence and strict equality**: with their help checking if the sum result is strictly equal to 0 and returns result as true

### Possible Refactors

This strategy could also be implemented with these Implementation ...

- `if/else` statement


---

## Notes

It's quite a simple challenge that helps to understand remainder operator better.