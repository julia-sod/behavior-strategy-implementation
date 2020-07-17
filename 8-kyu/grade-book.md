# [Grade-Book](https://www.codewars.com/kata/55cbd4ba903825f7970000f5)

This function checks the average of three given scores of a student and returns the letter value associated with that grade.

It can be used for deciding what letter value (A, B, C, D, E or F) a student has after passing an exam for example.

## Syntax

> getGrade(`number`) -> `string`

### Parameters

**s1, s2, s3**: `number`

- Three grades of students, that will be used to count an average grade.

### Return Value: `string`

The letter value (A, B, C, D, E or F) associated with the grade.

## Examples

This function's behavior is relatively simple to understand. This exercise didn't include complicated edge case. 


```js
const average = getGrade(90, 95, 100);
console.log(average)// "A"
```

```js
const average = getGrade(70,70,100);
console.log(average)// "B"
```

```js
const average = getGrade(70,70,70);
console.log(average)// "C"
```




## [shannagregory](https://www.codewars.com/users/shannagregory)

```js
function getGrade (s1, s2, s3) {
  const avg = (s1+s2+s3)/3;
  if (avg < 60)  return "F";
    else if (avg < 70) return "D";
    else if (avg < 80) return "C";
    else if (avg < 90) return "B";
    else return "A";
}
```

### Strategy

Shannagregory solved this problem by calculating the average of the given grades of a student and then decided which letter value it will be, according to the range.


### Implementation

The strategy was implemented with the help of conditional else/if statement that helps to decide into which range the average sum of the given parameters goes.

**if/else statement**: checks into which range the average goes and returns the letter value accordingly.

### Possible Refactors

This strategy could also be implemented with the following:

- conditional operator `?:`

---


## [jackzinn,](https://www.codewars.com/users/jackzinn)

```js
function getGrade (s1, s2, s3) {
  return ['F','F','F','F','F','F','D','C','B','A','A'][Math.floor((s1+s2+s3)/30)];
}
```

### Strategy

Jackzinn has a very interesting solution by putting all  possible results and finding the index according to average grade.

### Implementation

He puts an array with all the letter values and finds the right index with the help of Math.floor method.

**array**: all the possible answers are put into array.

**floor method**: counts the average and rounds a number downward to its nearest integer.

### Possible Refactors

This strategy could also be implemented with the following:

- `if else` statement;
- `switch`statement;
- `arrow function`



---

## Notes

I found second solution very elegant. It helped me to learn Math.floor method.
