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
<br>i - case-insensitive matching, so that it matches both uppercase and lowercase
<br>g - global matching that finds all matches in the input string, not just the first one
<br>m - multi-line matching, which allows '^' and '$'  to match the start and end of lines, not just the wholel string

### Grouping and Capturing
<br>(https?:\/\/) - This group is basically saying it allows the URL code to being with "http://", "https://" or none of them.
<br>([\da-z\.-]+) - This group which is the domain name. It matches 1 or more numbers, letters, dots or hypens. Ending it with a "+" linking it to the following line.
<br>([a-z\.]{2,6}) - Withe the + connecting this group together, this matches 2-6 copies of the sequences "[a-z\.]"
<br>([\/\w \.-]*) - This group is is being matched as many times as they want because of the "*" at the end. Basicallly acting like multiple directories. (refer back to Group project 2).

### Bracket Expressions
Expressions between "[]" brackets.

### Greedy and Lazy Match
Allow you to find the Greedy and Lazy Match.
<br>([\da-z\.-]+) 
<br>Greedy - longest
<br>Lazy - shortest
### Boundaries
Positions where a word starts or ends, and non-word are positions that are not words
<br>Represented by \b and /B
<br>/b - represents a word boundary
<br>\B - represents a non-word boundary

### Back-references
Allow you to refer back to a captured group in your regex pattern
\1, \2, etc.
<br>Will match words that are repeated

### Look-ahead and Look-behind
Look-ahead is represented by (?=pattern) for positive look-ahead (asserts that the pattern follows) and (?!pattern) for negative look-ahead (asserts that the pattern doesn't follow).
<br>Look-behind is represented by (?<=pattern) for positive look-behind (asserts that the pattern precedes) and (?<!pattern) for negative look-behind (asserts that the pattern doesn't precede).
<br>For example, if you want to match the word "apple" only if it is followed by "pie," you can use the pattern apple(?= pie).

### User Story
<br>AS A web development student
<br>I WANT a tutorial explaining a specific regex
<br>SO THAT I can understand the search pattern the regex defines

### Acceptance Criteria
<br>GIVEN a regex tutorial

<br>WHEN I open the tutorial.
<br>THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, 
<br>a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile.

<br>WHEN I click on the links in the table of contents.
<br>THEN I am taken to the corresponding sections of the tutorial.

<br>WHEN I read through each section of the tutorial.
br>THEN I find a detailed explanation of what a specific component of the regex does.

<br>WHEN I reach the end of the tutorial.
<br>THEN I find a section about the author and a link to the author’s GitHub profile.

## Author
Anthony Littlejohn
<br>www.github.com/ant05man
