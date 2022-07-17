Given a time in 12-hour AM/PM format, convert it to military (24-hour) time.

Note: - 12:00:00AM on a 12-hour clock is 00:00:00 on a 24-hour clock.
- 12:00:00PM on a 12-hour clock is 12:00:00 on a 24-hour clock

https://www.hackerrank.com/challenges/one-week-preparation-kit-time-conversion/problem?h_l=interview&isFullScreen=true&playlist_slugs%5B%5D=preparation-kits&playlist_slugs%5B%5D=one-week-preparation-kit&playlist_slugs%5B%5D=one-week-day-one&h_r=next-challenge&h_v=zen&h_r=next-challenge&h_v=zen

## Answer

```javascript
function timeConversion(s) {
    const getHour = timeInString => parseInt(timeInString.slice(0, 2))
  if(s.slice(-2) === 'AM'){
    return `0${getHour(s) == 12 ? 
    '0' : getHour(s)}` + s.slice(2, 8)
  }else{
     return `${getHour(s) !== 12 ? 
     getHour(s) + 12 : 12 }` + s.slice(2, 8) 
  }
}
```

## Hint
- parseInt is used to convert a string to number.
