# JavaScript Date Objects

## Date

JavaScript Date objects represent a single moment in time in a platform-independent format. Date objects encapsulate an integral number that represents milliseconds since the midnight at the beginning of January 1, 1970, UTC (the epoch).

## The epoch, timestamps, and invalid date

A JavaScript date is fundamentally specified as the time in milliseconds that has elapsed since the epoch, which is defined as the midnight at the beginning of January 1, 1970, UTC (equivalent to the UNIX epoch). This timestamp is timezone-agnostic and uniquely defines an instant in history.

he maximum timestamp representable by a Date object is slightly smaller than the maximum safe integer (Number.MAX_SAFE_INTEGER, which is 9,007,199,254,740,991). A Date object can represent a maximum of ±8,640,000,000,000,000 milliseconds, or ±100,000,000 (one hundred million) days, relative to the epoch. This is the range from April 20, 271821 BC to September 13, 275760 AD. Any attempt to represent a time outside this range results in the Date object holding a timestamp value of NaN, which is an "Invalid Date".

```JS

console.log(new Date(8.64e15).toString()); // "Sat Sep 13 275760 00:00:00 GMT+0000 (Coordinated Universal Time)"
console.log(new Date(8.64e15 + 1).toString()); // "Invalid Date"
```

There are various methods that allow you to interact with the timestamp stored in the date:

You can interact with the timestamp value directly using the getTime() and setTime() methods.
The valueOf() and [@@toPrimitive]() (when passed "number") methods — which are automatically called in number coercion — return the timestamp, causing Date objects to behave like their timestamps when used in number contexts.
All static methods (Date.now(), Date.parse(), and Date.UTC()) return timestamps instead of Date objects.
The Date() constructor can be called with a timestamp as the only argument.

## Date time string format

There are many ways to format a date as a string. The JavaScript specification only specifies one format to be universally supported: the date time string format, a simplification of the ISO 8601 calendar date extended format. The format is as follows:

YYYY-MM-DDTHH:mm:ss.sssZ

YYYY is the year, with four digits (0000 to 9999), or as an expanded year of + or - followed by six digits. The sign is required for expanded years. -000000 is explicitly disallowed as a valid year.
MM is the month, with two digits (01 to 12). Defaults to 01.
DD is the day of the month, with two digits (01 to 31). Defaults to 01.
T is a literal character, which indicates the beginning of the time part of the string. The T is required when specifying the time part.
HH is the hour, with two digits (00 to 23). As a special case, 24:00:00 is allowed, and is interpreted as midnight at the beginning of the next day. Defaults to 00.
mm is the minute, with two digits (00 to 59). Defaults to 00.
ss is the second, with two digits (00 to 59). Defaults to 00.
sss is the millisecond, with three digits (000 to 999). Defaults to 000.
Z is the timezone offset, which can either be the literal character Z (indicating UTC), or + or - followed by HH:mm, the offset in hours and minutes from UTC.


## MethoD Description

getFullYear()

- Get year as a four digit number (yyyy)

getMonth() 

- Get month as a number (0-11)

getDate()

- Get day as a number (1-31)

getDay() 

- Get weekday as a number (0-6)

getHours()

- Get hour (0-23)

getMinutes() 

- Get minute (0-59)

getSeconds() 

- Get second (0-59)

getMilliseconds() 

- Get millisecond (0-999)

getTime() 

- Get time (milliseconds since January 1, 1970)

