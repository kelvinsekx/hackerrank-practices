Given an array of integers, where all elements but one occur twice, find the unique element

https://www.hackerrank.com/challenges/one-week-preparation-kit-lonely-integer/problem?h_l=interview&isFullScreen=true&playlist_slugs%5B%5D%5B%5D=preparation-kits&playlist_slugs%5B%5D%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D%5B%5D=one-week-day-two

## Answer

```js
function getUniqueInt (arr) {
  return arr.find(each => a.indexOf(each) == a.lastIndexOf(each) )
}
```

## Highlight
- `lastIndexOf`: The lastIndexOf() method returns the last index at which a given element can be found in the array, or -1 if it is not present.
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/lastIndexOf
