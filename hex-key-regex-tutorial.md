# Regex Tutorial

A regex (regular expression) is a sequence of characters that allows for matching and location of designated text patterns. Regex's are typically used by string searching algorithms for find, find and replace, or input validation, such as password validation when establishing new user accounts on various applications. 

## Summary



This tutorial will be explaining the use of the hex key value regex `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`.

The tutorial will provide information regarding the hex key regex components, including: achoring, quantifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags, and character escapes.

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
`^` and `$` are the anchors that match the begging and the end of the line or string respectively. 

For instance, `^123`  will match any line or string that begins with 123 and `$456` will match any line or string that ends with 456.
### Quantifiers

The Hex Key regex uses the `?` and `{n}` quantifiers.

The `?` quantifier matches the character before it 0 or 1 times. This is also known as a non-greedy match. This means that in the hex key regex # can either be present or absent from the beginning of the string. 

For example: `/123?4` would find matches for 1234 and 124.

The `{n}` quantifier specifies an exact number of times to match the character before the quanitifier. This quantifier is used twice in the hex key regex. 

For example, `ABCDE{2}` will match strings that contain EE and `(ABCDE){2}` will match strings that contain ABCDE ABCDE
### Grouping Constructs

`()` is a grouping constructor. This will allow for capturing of anything matches that is contained within the constructors and quanitifiers to be applied to all characters within the constuctors. 

This can be referenced in the previous example for quantifiers `ABCDE{2}`
### Bracket Expressions

`[]` is a bracket expression that allows for a range of characters to be matched. f

For example, in our hex key regex, `[a-f0-9]` allows and requires matching of at least one alphanumeric characters between a-f and at least one numeric character 0-9.
### Character Classes
`a-f0-9` represent 2 seperate character classes (alphnumeric a-f and numeric 0-9 respectively). These classes will allow for the matching of on character within the set. 

`g-t` would allow a match of an alphanumeric character in the range of g and t.

### The OR Operator
`|` is the OR operator. This will allow for matching that meets either or set of conditions before or after the operator. 

For example. `Regex1|Regex2` would allow for matching of either Regex1 or Regex2.


## Author

[Christopher Stasney](https://github.com/cstasney)