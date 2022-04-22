# Matching an Email Regex Tutorial

This is a tutorial on the regular expression (regex) of an email to verify the user input is a valid email address

## Summary

The following is the code snippet of the regex of an email address.
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The regular expression of an email address has three parts: the local part,the '@' symbol, and the domain. The local part is a string limited by a collection of rules, the '@' symbol separates the local part from the domain, and the domain is a string of the web service of the email address. The parentheses '()' separate three different sets. 
The first character set or local part is shown by `([a-z0-9_\.-]+)` and is based on the rules of using lower case letters from a to z, number from 0 to 9, or special characters including '.' and '-'. The `_` matches a '_' character. The `\.` matches a '.' character.
The `@` matches a '@' character. 
The second character set is shown by `([\da-z\.-]+)`. The `\d` matches a single character that is a digit. It is a shorthand of 0-9 which was shown in the first character set. 
The third character set is shown by `([a-z\.]{2,6})` with the characters between 2 and 6 characters and be any letter from a to z or special character.
The `\.` is to match a '.' character. 

## Table of Contents

- [Matching an Email Regex Tutorial](#matching-an-email-regex-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Character Classes](#character-classes)
    - [Flags](#flags)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
  - [Author](#author)

## Regex Components

### Anchors
`/^...$/`
The anchors in the email address regex can be shown by the symbols '^' and '$'
The '^' symbol asserts its position at the start of the string and the string begins.

### Quantifiers
`+`
`{2,6}`
The quantifiers in the email address can be shown by the symbol of '+' and '{}' 
The '+' symbol is another 1 to infinity quantifier. It means it matches one or more times.
The '{}' symbol means the lowercase letters and the symbols '\' and '.' should match a string the user inputs at least 2 times but no more than 4 times.

### Character Classes
`\d`
The character class in the email address can be shown by `\d`
The 'd' matches with at least one digit from 0 to 9. In other words, `\d` is short for [0-9].

### Flags
`/.../`
The flags in the email address can be shown by the symbol of a slash '/'
The '/' symbol signifies the start and end of the expression. The flags in the email regex is a multiline flag, which makes '^' match the start of the line and the '$' match the end of the line. 

### Grouping and Capturing
`([a-z0-9_\.-]+)`
`([\da-z\.-]+)`
`([a-z\.]{2,6})`
The parentheses in the email address are ways of grouping and capturing certain groups. 

### Bracket Expressions
`[a-z0-9_\.-]`
`[\da-z\.-]`
`[a-z\.]`
The bracket expressions in the email address can be shown by the symbol of brackets '[]'
Within the brackets are characters that must match with any characters the user inputs. The requirements of characters are explained in the "Summary" section. 

## Author
https://gist.github.com/hannahhan153/78744d8cc64ea45a2999d7cfa5a0cbc8 
https://github.com/hannahhan153/Regex-Tutorial 
