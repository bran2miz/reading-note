# Reading 19 - Automation

## Python Regular Expressions Tutorial

**Regular Expressions** - Regex - sequence of characters to check if a pattern exists in a given string of text or not.
-validates format of email addresses or passwords during registration
-parse text data
-helps manipulate textual data

## Regex Tutorial

-import re - Python library for regex.

Basic Pattern

-match() function - returns a "match" object if text matches the pattern. Else returns none.

-r in the beginning of a string text is the *raw string literal*

-raw string literal - changes how string literal is interpreted.

## Wild Card Characters

- **search()** - scan through string/sequence looking where the regex produces a match.

- **group()** - returns string matched by the re. 

**.** - period that matches any single character except the newline character.

**^** - caret that matches start of string.

**$** - matches end of string.

**[abc]** - matches a or b or c

**[a-zA-Z0-9]** - matches later from (a to z) or (A to Z) or (0 to 9)

\ - backslash
-if a character following backslash is a recognized escape character then special meaning of term is taken.
-else the character following the backslash isn't an escape character, then the backslash is seen as an ordinary character and parsed through.

**\w** - lowercase 'w'. Matches any single letter, digit, or underscore.

**\W** - uppercase 'W'. matches any character not part of lowercase W.

**\s** - lowercase 's'. Matches a single whitespace character like space, newline, tab, and return.

**\S** - uppercase 'S'. matches any character not part of lowercase s.

**compile()** - computer a regex pattern into a regex object

**findall()** - finds all possible matches in entire sequence and returns them as a list of strings.

**finditer()** - finds all possible matches in entire sequence but returns regex match objects as an iterator.

**sub()** - substitute function
-returns string obtained by replacing or substituting the left most occurrences of pattern id string.

**split()** - splits string wherever the pattern matches and returns a list.

## Compilation Flags

**IGNORECASE(I)** - Allows case - sensitive matches.

**DOTALL(S)** - allows to match any character, including new line.

**MULTILINE(M)** - Allows start of string (^) and end of string ($) anchor to match newlines as well.

**VERBOSE(X)** - Allows you to write whitespace and comments within regular expressions to make it more readable.

## Shutil - High Level Files Operations

shutil module includes high-level operations such as copying and archiving.

copyfile() - copies content of source to the destination and raise IDError if it doesn't have permission to write destination file.

### Working with Directory Trees

shutil includes three functions for working with directory trees.

**copytree()** - to copy a directory from one place to another
-recurses through source directory tree, copying files to the destination.

### Finding Files

**which()** - function that scans a search path looking for a named file.
-Goal: to find executable program on shells search path defined in environment variable path.

### Archives

-python standard library includes many modules for managing archive file.
-**shutil.get_archive_format()** - returns a sequence of names and descriptions for formats supported on current system.
