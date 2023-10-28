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

Grouping constructs are used to verify different requirements within parts of the string. The most commonly used construct is called a subexpression. This is declared by using parentheses () and are used to find an exact match within the string. To look for an exact match between 2 or more strings you would have to use a colon : to seperate your strings.

e.x:
(grouping):(constructs) will not match to (grouped):(constructs)

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

Character classes are used to define what individual symbols and characters can represent. They are used to simplify ways of fulfilling matches within our string. Lets go over all of the different character classes within our regex.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

- a-z: Matches any lowercase letter from a-z
- 0-9: Matches any digit from 0-9
- \_: Matches an underscore
- \.: Matches a period
- -: Matches a hyphen
- \d: Matches any digit from 0-9

You may be thinking I left one out however, the @ symbol is not a character class but a literal match for the at symbol.

### The OR Operator

The OR operator seperates how the search is structured and matched.

Example:

(o|n|e):(t|w|o)

"one:two" and "eon:wot" would now both match using an OR operator however "two:one" would not.

### Flags

Flags are used with a single lowercase character and are placed after the expression pattern. Here are the six different flags you can use.

- g (global): Regular expressions stop searching after finding the first match for a pattern. The g flag makes the regex find all matches for the pattern in the string and not just the first.

- i (ignore case): Regular expressions perform a case sensitive search. The i flag makes the search non case sensitive.

- m (multline): The m flag is used when you want to match the search to multiple lines.

- u (unicode): The u flag makes the regular expression assume the string is a sequence of unicode.

- y (sticky): The y flag tells the expression to perform sticky matching in the target string.

- s (dotAll): The s flag makes the dot (.) character match with all characters including newline characters (\n)

### Character Escapes

Character escapes in regex are exactly what the name implies. The backslash \ is used to stop the search from interpreting a character literally.

Take this line of code for example: ([\da-z\.-]+)

If this sequence failed to have a backslash in front of the d then the search would look literally look for a lowercase d. However since the slash is placed before it the search knows that truly means to match every digit from 0-9.

## Author

My name is Gabriel Rinaldi and I'm a 21 yr old from California. I recently just moved to the great state of Utah where I plan to pursue a career in web devolopment. Here's a link to find more of my work! - https://github.com/gaberinaldi
