# Regular Expressions

Regular expressions, or regex, are an advanced way to search strings of text. They use a sequence of characters define a search pattern. A regex can then be used within a javascript function to find exact matches to the criteria. In this tutorial I will show an example of a regular expression, explain all the different components, and then break down the function of the regular expression.

## Summary

This tutorial will discuss the following regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. This regex looks for a valid email address in a string.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Boundaries](#boundaries)
- [Breakdown](#breakdown)

## Regex Components

### Anchors
Anchors are used to match a position in the string. The four most common anchors are:
- `^` => The beginning of the string
- `$` => The end of the string
- `\b` => The boundary of a word within the string (space, punctuation, line break, etc.)

### Quantifiers
Quantifiers are used to indicate how many characters for the regex to match. They are by default "greedy" and will match as many as possible. Some common quatifiers are:
- `+` => This means look for one or more
- `*` => This means look for zero or more. 
- `{x,y}` => Look for a range of matches between x and y
- `{n}` => Look for n number of matches
= `?` => Look for 0 or 1. This quatifier can also be used after another quantifier to override the default behavior and make the quantifier "lazy".

### Character Classes
Character classes are used to define what characters the user is searching for. There are two types of character class. First there are several predefined classes and second there user defined classes.

Some common predefined classes are:
- `.` => Match anything
- `\d` => Any number 0 through 1
- `\w` => Match any alphanumeric or underscore
- `\s` => Match any white space

User defined classes are written within square brackets and can be used when one of the predefined classes. For example if you wanted to search for a number between 1 and 5 you would write `[1-5]`. Or if you wanted to search for lowercase "a" through "z" or a number you would write `[a-x0-9]`.

### Grouping and Capturing
Groups are used to capture specific part of the regular expression. This is helpful for advanced search and replace functions. A group is indicated using parentheses.

### Boundaries
Regular expressions are bounded by `//`.

### Breakdown
So let's break down the following regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.
First the `/` indicates the start of the regex. Next the `^` says to start the search at the beginning of the string. Next you have the beginning of the first group. Inside this group is a class that is looking for one or more, as indicated by the `+`, of characters "a-z", "0-9", "_", ".", or "-". The expession is then looking for that group to be followed by the literal "@" symbol. Then it starts and new group with a new character class. This time is is looking for more that one of any combination of numbers and letter followed by a period. Also in this case the period is included in the second group. Then, there is a third group with a third user defined character class. This time it is looking for any combination of numbers, letters, or periods, 2 to 6 characters long. Lastly, there is a `$` to indicate the end of the string and a second `/` to indicate the end of the regex.

## Author

My name is Caleb Korson and I am currently enrolled in Vanderbilt's Coding Bootcamp.

[Github Profile](https://github.com/ckkorson)

Email Address: [caleb.k.korson@gmail.com](mailto:caleb.k.korson@gmail.com)
