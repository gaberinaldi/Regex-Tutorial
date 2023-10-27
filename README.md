# Regex Tutorial

Regex, also known as regular expression is a series of special characters that validates a search pattern based on several given requirements.

## Summary

The regex I will be describing will be used to match an email. I will explain all of the requirements that are needed to validate this search pattern and what each special character means.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

The two anchers displayed in our regex are ^ and $. The ^ symbol represents a string that begins with the characters following the symbol. So for our regex that would be [a-z0-9_\.-]. The $ symbol represents a string that ends with the characters prior to it. In our regex this would be [a-z\.]. {2,6} is not included because it is a quantifier

### Quantifiers

Quantifiers set the boundaries on the string that the regex is matching.

The way our pattern is structured {2,6}, only allows it to match with a string with a minumum of 2 characters and a maximum of 6.

### Grouping Constructs

### Bracket Expressions

Bracket expressions [], are used to validate a search pattern. They are used to match any characters or symbols that are stated within the brackets.

Take a look at how to break down the given bracket expressions below:

[a-z0-9_\.-]

- a-z: Matches any lowercase letter from a-z
- 0-9: Matches any digit from 0-9
- \_: Matches an underscore
- \.: Matches a period
- -: Matches a hyphen

[\da-z\.-]

- \d: Matches any digit from 0-9
- a-z: Matches any lowercase letter from a-z
- \.: Matches a period
- -: Matches a hyphen
  In conclusion this bracket expression will match any single digit, lowercase letter, period, or hyphen.

[a-z\.]

- a-z: Matches any lowercase letter from a-z
- \.: Matches a period

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
