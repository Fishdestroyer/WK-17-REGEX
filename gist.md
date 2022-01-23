# WEEK 17 REGEX

## Description

In our week 17 assignment, we are tasked with breaking down a REGEX (Regular Expression) and describing each section of the expression.

## Summary

I have chosen to use one of the supplied expressions from our module content, matching an email.
 The supplied expression is as follows-
 
  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Acceptance criteria

GIVEN a regex tutorial

WHEN I open the tutorial

THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the 
regex featured in the tutorial, a table of contents linking to different sections that break down each component of the
regex and explain what it does, and a section about the author with a link to the author’s GitHub profile

WHEN I click on the links in the table of contents

THEN I am taken to the corresponding sections of the tutorial

WHEN I read through each section of the tutorial

THEN I find a detailed explanation of what a specific component of the regex does

WHEN I reach the end of the tutorial

THEN I find a section about the author and a link to the author’s GitHub profile

## Technologies and language

- Markdown

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
- Anchors do not match any character rather they match positions bfore the begining, at the end or between characters. In 
the above string, the anchors, (^) and ($), are in the begining and end positions.

### Quantifiers
- Quantifiers match a number of instances of a character, goup or character class in a string.
- examples include - Exact Count {n}, The range {n, m}, and shorthand +, ?, *. 
- For the above string, the expression [a-z.]{2,6} matches between 2 to 6 copies of the sequence found inside of the square brackets.

### OR Operator
- The OR operator is represented by "|" and can be used to specify a case (upper or lower) i.e. B\b. 
- In the above string, there is no call for the or operators use.

### Character Classes
Character classes are also referred to as character sets. The regex engine will only match one of several characters, just 
place the characters you want to match inside of square brackets []. By using a hyphan, you can specifiy a range you want to search 
with your character class. You can also use more than one range in the same square brackets.

- Expamles - to search for an a or e [ae], range [0-5] multiple range [0-5 t-z T-Z]

Examples in this string
- a-z0-9 matches lowercase letters a-z and numbers 0-9

### Grouping and Capturing


### Bracket Expressions
Brackets indicate a set of charachters to match. This can consist of an individual character or a set of characters with the use of a hyphen.
The use of metacharacters can negate what is between brackets.

Examples
-'dog'.match(/[abcd/]) -> matches 'd', 'donkey'.match(/[^abcd]/) -> matches 'o'
The outcome of each bracket expression depends on the brackets/ braces used- {}, [], ()
Examples in this string
-[a-z0-9_.-]
-[\da-z.-]
### Greedy and Lazy Match
A Greedy match equates to as many as possible, where lazy is quite the opposite and looks for as little as possible when matching strings and tokens.
This does not apply to the above string. 

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Credits and additional research

- Starter code providded 
- MDN- 
- DOCS.Microsoft
- https://www.regular-expressions.info/
- https://www.javascripttutorial.net/


## Author

Authored by Jeff Whitner, please see previous section "Credits" for additional assistance information.

https://github.com/Fishdestroyer