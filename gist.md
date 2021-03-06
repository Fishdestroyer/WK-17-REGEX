# WEEK 17 REGEX

## Description

In our week 17 assignment, we are tasked with breaking down a REGEX (Regular Expression) and describing each section of the expression.

## Summary

I have chosen to use one of the supplied expressions from our module content, matching an email.
 The supplied expression is as follows-
 
  /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
  
    Given the above expression, when matched to the following

  -email21@email.com

  ^- begining of the string
  
  ([a-z0-9_\.-]+)- Capturing group 1 with quantifier "+" for 1 or more of the preceding token.- Is looking for the a-z and 0-9 range, case sensitive "email21"

  @ Matches a "@" character - "@"

  ([\da-z\.-]+)\. - Capturing group 2 with quantifier "+" for 1 or more of the preceding token. Is looking for digit match and a-z range, case sensitive "email"
  
  \. Matches a "." character - "."

 ([a-z\.]{2,6}) - Capturing group 3 with quantifier {2,6} to match between 2 and 6 of the preceding token "com"
 
 Quantifier examples include  .co, .com, .gov, .org up to 6 characters.

 $- closing of string

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

## GitHub Gist


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)


## Regex Components

### Anchors
- Anchors do not match any character rather they match positions before the begining, at the end or between characters. In 
the above string, the anchors, (^) and ($), are in the begining and end positions.

### Quantifiers
- Quantifiers match a number of instances of a character, goup or character class in a string.
- examples include - Exact Count {n}, The range {n, m}, and shorthand +, ?, *. 
- For the above string, the expression [a-z.]{2,6} matches between 2 to 6 copies of the sequence found inside of the square brackets.

### Character Classes
Character classes are also referred to as character sets. The regex engine will only match one of several characters, just 
place the characters you want to match inside of square brackets []. By using a hyphan, you can specifiy a range you want to search 
with your character class. You can also use more than one range in the same square brackets.

- Expamles - to search for an a or e [ae], range [0-5] multiple range [0-5 t-z T-Z]

Examples in this string
- a-z0-9 matches lowercase letters a-z and numbers 0-9

### Grouping and Capturing

Groups multiple tokens together and creates a capture group for extracting a substring or using a backreference.

Example
/(ha)+/
hahaha haa hah!

ALL ha would match, leaving singular characters "a" and "h" unmatched as they are not of a pair. hahaha would match because of the "+"
quantifier.

Examples in this string
- [a-z0-9_.-]+)
- ([\da-z.-]+)
- ([a-z.]{2,6})


### Bracket Expressions
Brackets indicate a set of charachters to match. This can consist of an individual character or a set of characters with the use of a hyphen.
The use of metacharacters can negate what is between brackets.

Examples
-'dog'.match(/[abcd/]) -> matches 'd', 'donkey'.match(/[^abcd]/) -> matches 'o'

The outcome of each bracket expression depends on the brackets/ braces used- {}, [], ()

Examples in this string
-[a-z0-9_.-]
-[\da-z.-]

## Credits and additional research

- Starter code provided 
- Shawn Littrell, TA
- MDN- 
- DOCS.Microsoft
- https://www.regular-expressions.info/
- https://www.javascripttutorial.net/
## Author

Authored by Jeff Whitner, please see previous section "Credits" for additional resources used.

https://github.com/Fishdestroyer