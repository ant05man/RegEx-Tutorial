# RegEx-Tutorial

A regular expression (Regex/Regexp), is a special text string for describing a search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string.

## Summary

This will be a tutorial explaining how a regular expression functions and we will break down each part of the expression.

## Example

For example, the following regular expression can be used to verify that user input is a valid email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Always at the begining and the end of the string.
^ - Matches any string that starts with
$ - Matches a string that ends with

### Quantifiers
Quantifiers communicate to the regex engine that it MUST match the quantity of the character or expression to its left. Two type of quantifiers are Greedy and Lazy

### OR Operator
Represented by the vertical bar '|'. Used to match either of two patterns
apple|banana

### Character Classes
[a-z] - Matches lowercase alphabetic characters between a and z
<br>\w - Matches a single word
<br>\d - Matches a single character that is a digit 0-9
<br>. - Matches any character

### Flags
Used to modify how the pattern is matched
i - case-insensitive matching, so that it matches both uppercase and lowercase
g - global matching that finds all matches in the input string, not just the first one
m - multi-line matching, which allows '^' and '$'  to match the start and end of lines, not just the wholel string

### Grouping and Capturing
(https?:\/\/) - This group is basically saying it allows the URL code to being with "http://", "https://" or none of them.
([\da-z\.-]+) - This group which is the domain name. It matches 1 or more numbers, letters, dots or hypens. Ending it with a "+" linking it to the following line.
([a-z\.]{2,6}) - Withe the + connecting this group together, this matches 2-6 copies of the sequences "[a-z\.]"
([\/\w \.-]*) - This group is is being matched as many times as they want because of the "*" at the end. Basicallly acting like multiple directories. (refer back to Group project 2).

### Bracket Expressions
Expressions between "[]" brackets.

### Greedy and Lazy Match
Allow you to find the Greedy and Lazy Match.
([\da-z\.-]+) 
Greedy - longest
Lazy - shortest
### Boundaries
Positions where a word starts or ends, and non-word are positions that are not words
Represented by \b and /B
/b - represents a word boundary
\B - represents a non-word boundary

### Back-references
Allow you to refer back to a captured group in your regex pattern
\1, \2, etc.
Will match words that are repeated

### Look-ahead and Look-behind
Look-ahead is represented by (?=pattern) for positive look-ahead (asserts that the pattern follows) and (?!pattern) for negative look-ahead (asserts that the pattern doesn't follow).
Look-behind is represented by (?<=pattern) for positive look-behind (asserts that the pattern precedes) and (?<!pattern) for negative look-behind (asserts that the pattern doesn't precede).
For example, if you want to match the word "apple" only if it is followed by "pie," you can use the pattern apple(?= pie).

## Author
Anthony Littlejohn
www.github.com/ant05man
