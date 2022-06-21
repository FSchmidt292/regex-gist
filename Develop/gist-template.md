# Regex Breakdown

This is my challenge for week 17, interpretting a line of Regex code and breaking it down, explaining exactly what the piece of code is checking against. I will breakdown portions of a regex line and explain each piece of the code to demonstrate an understanding of what is going on with the code.

## Summary

I have selected to breakdown the regex for matching a hex value. This is the code snippet:

"/^#?([a-f0-9]{6}|[a-f0-9]{3})$/"

I will be breaking down each individual element here and also explaining what the specific fields are looking for (ex, entire alphabet or just a portion of the alphabet).

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components
This regex string contains several components. The string uses anchors, Quantifiers, an OR operator, Grouping and Capturing, and Bracket Expressions. They will be highlighted and broken down in their specific section on this page. 

### Anchors
The only Anchor in this Regex string is at the beginning. Since hex values will always begin with an Octothorpe for CSS, the start of this string begins with the anchor symbol followed by an Octothorpe.

### Quantifiers
After the initial Octothorpe Anchor, there is a ? quantifier. This is here to match 0-1 of the Octothorpe, meaning that it will match if there is no Octothorpe, or if there is. This is likely because the Hex Number may be present but not used for CSS purposes, so if there isn't an Octothorpe present, it will still get picked up as long as it fits the rest of the Hex profile.

There is a quantifier behind [a-f0-9], it is {6}. This quantifier is dictating that there will be 6 preceding matches which will follow the dictated character range of a-f and 0-9. there is another curly bracketed quantifier after the OR operation which is {3}, which is doing the same thing, if there is not 6 that match a-f 0-9, there will be 3 matches.

### OR Operator
Our OR operator sits between the two options for our hex number. Hex values can either be 3 digit or 6 digit, so this OR operator, the "|" between the first character set and the second character set, is used to make it so that it searches for one or the other and doesn't exclude either option.

### Grouping and Capturing
The parenthesis surrounding nearly the entire expression are our capture group. The capture group includes the OR operator as well because it is within the same capture field. We are looking for a single value, either 3 or 6 characters in length. We need to include everything in the capture field in this instance because if we don't, the OR operator is going to 

### Bracket Expressions
The Bracket Expressions in this string are [a-f0-9]. This is written in this way because the hex value can contain or exclude the alphabetic characters abcdef, or the numeric characters 123456789. We don't care the order that these characters will appear in since they can be any and still be valid Hex values, we simply describe what they can possibly be here. 


## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)