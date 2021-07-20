# A Regex Tutorial guide


## Brief Summary:
- Regex are regular expressions that are assigned an alternate contextual value.
- Regex include but are not limited to: Anchors, Constructs, Escapes, etc.



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
```
^The        matches any string that starts with The -> Try it!
end$        matches a string that ends with end
^The end$   exact string match (starts and ends with The end)
roar        matches any string that has the text roar in it
```

### Quantifiers
```
abc*        matches a string that has ab followed by zero or more c -> Try it!
abc+        matches a string that has ab followed by one or more c
abc?        matches a string that has ab followed by zero or one c
abc{2}      matches a string that has ab followed by 2 c
abc{2,}     matches a string that has ab followed by 2 or more c
abc{2,5}    matches a string that has ab followed by 2 up to 5 c
a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc
```
### Grouping Constructs
```
a(bc)           parentheses create a capturing group with value bc -> Try it!
a(?:bc)*        using ?: we disable the capturing group -> Try it!
a(?<foo>bc)     using ?<foo> we put a name to the group -> Try it!
```
### Bracket Expressions
```
[abc]            matches a string that has either an a or a b or a c -> is the same as a|b|c -> Try it!
[a-c]            same as previous
[a-fA-F0-9]      a string that represents a single hexadecimal digit, case insensitively -> Try it!
[0-9]%           a string that has a character from 0 to 9 before a % sign
[^a-zA-Z]        a string that has not a letter from a to z or from A to Z. In this case the ^ is used as negation of the expression -> Try it!
```
### Character Classes
```
\d         matches a single character that is a digit -> Try it!
\w         matches a word character (alphanumeric character plus underscore) -> Try it!
\s         matches a whitespace character (includes tabs and line breaks)
.          matches any character -> Try it!
```
### The OR Operator
```
a(b|c)     matches a string that has a followed by b or c (and captures b or c) -> Try it!
a[bc]      same as previous, but without capturing b or c
```
### Flags
```
g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)

```
### Character Escapes
```
\t  non printable tabs in a text block
\n  new-lines 
\r carriage returns .
```
## ESCAPES EXAMPLES
`/ [ . * + ? ^ $ {  } ( ) | [ \ ] \ \ ] /  g`


## ESCAPES APPLICATION

`( "Practice 578".match(/\d\.\d/) ); `


## Authors / Resources
Credits to: 
- https://www.w3schools.com/jsref/jsref_obj_regexp.asp
- https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions
