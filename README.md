# MongoDB $inc operator error with string value
This repository demonstrates a common error when using the `$inc` operator in MongoDB update queries. The `$inc` operator is used to increment a numerical field by a specified value. However, if you provide a string value, MongoDB will throw an error.

## Bug
The bug is in the `updateOne` query, which uses the `$inc` operator to increment the `field` with the value 'abc', which is a string. This leads to an error because `$inc` requires a number.

## Solution
The solution is to provide a numerical value to the `$inc` operator. The corrected query increments the `field` with the value 1.