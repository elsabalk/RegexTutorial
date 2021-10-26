# Matching an Email Regex Tutorial
This tutorial is a simple introduction to regular expressions, also known as a regex. A regex is a sequence of characters that is used to form a search pattern. 

## Summary
I will be going over a common regex, matching an email. The following is a regex for matching an email:  `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors signify the start and/or end of a string. Some of the most commonly user Anchors are:
`^` (caret): This anchor matches at the start of a string within a regex pattern.
`$` (dollar): This anchor matches the end of a string within a regex pattern.

You can see the anchors in the beginning and end of my email example: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Quantifiers
Qunantifiers are used to specifiy the number of instances of a character or group that should be matched within a regex pattern.Some of the most commonly user Qunantifiers are:

`{n}`: This quantifier matches exactly n times, n being an integer value.
`{ n ,}`: This quantifier matches at least n times, n being an integer value.
`{ n , m }`: This quantifier matches from n to m times, both being integers.
`?`: This quantifier matches 0 to 1 times.
`+`: This quantifier matches 1 or more times.
`*`: This quantifier mataches 0 to more times.

You can see in the third grouping of the email example it is looking for between 2 and 6 characters: `([a-z\.]{2,6})`

### Grouping Constructs
Grouping Constructs are used to create a sub-expression by placing an expression inside matching open and close parentheses. This is basically placing a part of a regex inside parentheses to group it together. 

My email example has three groupings:
`([a-z0-9_\.-]+)`
`([\da-z\.-]+)`
`([a-z\.]{2,6})`

### Bracket Expressions
Using brackets, `[]`, in a regex will search for any of the characters or digits within the brackets.

In the email example, the first grouping `([a-z0-9_\.-]+)` is searching for lowercase letters a through z, digits 0 through 9, underscores, periods, and dashes. The second grouping `([\da-z\.-]+)`is looking for and digit 0 through 9, lowercase letters a through z, and periods and dashes. The third grouping `([a-z\.]{2,6})` is searching for lower case letters a through z (between two and six characters).

### Character Classes
A character class matches a character from a certain set of characters. For instance `[0-9]` will match with any digits 0 through 9. Another example would be `[a-z]`, this will match any lowercase letter a through z. In the email example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` you can see where it is looking for letters a-z, and digits 0-9.

### The OR Operator
The OR operator, also know as alternation, is probably one of the easier regex concepts to grasp. It uses the `|` (pipe) symbol, and simply tells the regex to search for the character before or after the |. For example, if you were looking for the word artifact (correct American English spelling) you could use a regex `[art(i|e)fact]` to also include British spelling. 

### Flags
A flag can be added on to the end of a regex for additional functionality. There are three main regex flags:
`i`: This performs a search that is not case-sensitive.
`g`: This performs a global search and will find all instances, rather that stopping at the first instance.
`m`: This performs a multi-line search.

### Character Escapes
Certain characters have special meaning in regular expressions, but if you need to find them literally, you can use the character by putting a backslash `\` in front of it.

The email example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` has three instances of escaping the period to find literal periods.

## Author
My name is Elsa Balkaran. You can find more of my work at https://github.com/elsabalk.

