# Chameleon Site
This is a very simple script to change the site's background color from `fromColor` to `toColor` over a period of `maxDays`. The default starting date is 1 Jan 2023.

## Parameters
`maxDays`: Integer value to determine how many days over the change should take place.
`fromColor`: An object with properties `r`, `g` and `b`, all integers from 0 to 255 to determine the starting color.
`toColor`: An object with properties `r`, `g` and `b`, all integers from 0 to 255 to determine the ending color.

## Procedure
1. Set Start Date to 1 Jan 2023, `startDate`.
2. Get Current Date, `currentDate`.
3. Determine number of days difference between `startDate` and `currentDate`, `days`.
4. Declare `finalColor` and set it to the value of `toColor`. `finalColor` is the value that will ultimately be the site's background color. At the end of this script, it will be anywhere between `fromColor` to `toColor`, inclusive.
5. If `days` is more than or equal to `maxDays`, do nothing and skip straight to step 11.
6. Determine `ratio` by dividing `days` by `maxDays`. Get the whole number.
7. Get the different of the `r` property of `fromColor` and the `r` property of `toColor`, `rDiff`.
8. Multiply `rDiff` by `ratio` and add the result to the `r` property of `fromColor`.
9. Assign the result to the `r` property of `finalColor`.
10. Repeat steps 7 to 9 for the `g` and `b` properties.
11. Use `finalColor` to set the background of the website.
