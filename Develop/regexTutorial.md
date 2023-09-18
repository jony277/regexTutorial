# Matching an Email - Regex Tutorial

## Summary

In this tutorial, we will explore the regular expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` and understand how it can be used to validate email addresses. We'll break down each component of the regex and provide examples to demonstrate its functionality.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Author](#author)

## Regex Components

### Anchors
The `^` and `$` symbols in the regex serve as anchors. The `^` anchor signifies the start of the string, while the `$` anchor indicates the end of the string. In our regex, they ensure that the email address matches from start to finish.

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Example:

Valid: john.doe@example.com
Invalid: invalid.email@

### Quantifiers
Quantifiers specify how many times a character or group should appear. In our regex, + and {2,6} are quantifiers. + means that the preceding character group must appear at least once, and {2,6} specifies that the domain extension should consist of 2 to 6 characters.

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Example:

Valid: john.doe@example.com
Invalid: j@example.c

### Grouping Constructs
Parentheses () are used for grouping in regex. In our regex, we have three groups:

([a-z0-9_\.-]+): Matches the username part of the email address.
([\da-z\.-]+): Matches the domain name.
([a-z\.]{2,6}): Matches the top-level domain (TLD).

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Example:

Valid: john.doe@example.com
Invalid: john.doe@.com

### Bracket Expressions
Bracket expressions [...] specify a character set. In our regex, [a-z0-9_\.-] matches lowercase letters, digits, underscore, period, and hyphen.

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Example:

Valid: john.doe@example.com
Invalid: JohnDoe@example.com

### Character Classes
Character classes like \d represent predefined sets of characters. In our regex, [\d] matches digits (0-9).

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Example:

Valid: jane123@example.com
Invalid: jane@example.com

### The OR Operator

The | symbol acts as an OR operator, allowing multiple patterns to match. In our regex, we use it to match either a six-character or three-character TLD.

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Example:

Valid: john.doe@example.com
Valid: jane@example.co

### Flags
Flags can be added to the regex to modify its behavior. Common flags include i for case-insensitive matching, but our regex doesn't require any flags.

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Character Escapes
Backslashes \ are used to escape special characters. In our regex, we escape the period . to match it literally.

```regex
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
Example:

Valid: jane.doe@my-domain.co

## Author
This tutorial was created by Jonathan Gutierrez
[GitHub Profile](https://github.com/jony277)
