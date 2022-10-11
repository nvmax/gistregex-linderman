# Password Strength Validation - Regex

Tutorial to explain how to use regluar expression to validate a password strength.

## Summary
Using the following rules: 

The password must contain at least one uppercase letter, one lowercase letter, one number, one special character and must be at least 8 characters long.

/^(?=.*[A-Z].*[A-Z])(?=.*[a-z].*[a-z].*[a-z])(?=.*[0-9].*[0-9])(?=.*[!@#$%&*]).{8,}$/

Using the rules above, the following passwords are valid:

    * Password1!
    * PaSSword1@
    * Pa$$w0rd1!
    * P@ssw0rd1!
    * P@$$w0rd1!


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

Anchors are used to match a pattern at the beginning or end of a string.

The `^` and `$` characters are used to match the beginning and end of a string respectively.




### Quantifiers

Quantifiers are used to specify the number of occurrences of a character, group or character class that must be present in the input string for a match to be found.

The `*` quantifier matches zero or more occurrences of the preceding expression.

The `+` quantifier matches one or more occurrences of the preceding expression.

The `{n}` quantifier matches exactly n occurrences of the preceding expression.

The `{n,}` quantifier matches n or more occurrences of the preceding expression.

Examples:  

            * `a*` matches zero or more occurrences of the character `a`.
            * `a+` matches one or more occurrences of the character `a`.
            * `a{2}` matches exactly two occurrences of the character `a`.
            * `a{2,}` matches two or more occurrences of the character `a`.
            * `a{2,4}` matches two, three or four occurrences of the character `a`.



### Grouping Constructs

Grouping constructs are used to match a sequence of characters.

The `()` grouping construct is used to match a sequence of characters.

Examples:

            * `(abc)` matches the characters `abc` in that order.
            * `(a|b)` matches either `a` or `b`.
            * `(a|b)*` matches zero or more occurrences of either `a` or `b`.




### Bracket Expressions

Bracket expressions are used to match a single character out of several possible characters.

The `[]` bracket expression is used to match a single character out of several possible characters.
using `^` inside the brackets will negate the expression, so it will match any character that is not in the brackets.

Examples:  

            * `[abc]` matches the characters `a`, `b` or `c`.
            * `[a-z]` matches any lowercase letter.
            * `[A-Z]` matches any uppercase letter.
            * `[0-9]` matches any digit.
            * `[a-zA-Z0-9]` matches any alphanumeric character.
            * `[^abc]` matches any character except `a`, `b` or `c`.
            * `[^a-z]` matches any character except a lowercase letter.
            * `[^A-Z]` matches any character except an uppercase letter.
            * `[^0-9]` matches any character except a digit.
            * `[^a-zA-Z0-9]` matches any character except an alphanumeric character.
            * `[a-z&&[def]]` matches the characters `d`, `e` or `f`.
            * `[a-z&&[^bc]]` matches any lowercase letter except `b` or `c`.
            * `[a-z&&[^m-p]]` matches any lowercase letter except `m`, `n`, `o` or `p`.
            * `[!@#$%&*] matches any of the characters `!`, `@`, `#`, `$`, `%`, `&` or `*`.


        

### Character Classes

Character classes are used to match a single character from a predefined set of characters. the first character you see in the character class is the negation character `^` which means that the character class will match any character that is not in the set.

The `.` character class is used to match any single character except a newline character.

* The following example matches a single character that is an uppercase letter `[A-Z]`.

* the following example matches a single character that is a lowercase letter `[a-z]`.

* The following example matches a single character that is either a number`[0-9]`.

* the following example matches a special character `[!@#$%&*]`.



### The OR Operator

The `|` OR operator is used to match one of several expressions.

Examples of OR operator:

            * `a|b` matches either an `a` or a `b`.
            * `a|b|c` matches either an `a`, a `b` or a `c`.
            * `a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z` matches any lowercase letter.
            * `A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z` matches any uppercase letter.
            * `0|1|2|3|4|5|6|7|8|9` matches any digit.
            * `!|@|#|$|%|^|&|*` matches any of the characters `!`, `@`, `#`, `$`, `%`, `^`, `&` or `*`.



### Flags

Flags are used to modify the behavior of a regular expression.

The `g` flag is used to perform a global match (find all matches rather than stopping after the first match).

The `?=...` flag is used to perform a positive lookahead.

Examples: 

            * `/a/g` matches all occurrences of the character `a` in the string.
            * `/a/gi` matches all occurrences of the character `a` in the string ignoring case.
            * `/a(?=b)/` matches the character `a` only if it is followed by the character `b`.
            * `/a(?=b)/g` matches all occurrences of the character `a` only if it is followed by the character `b`.



### Character Escapes

Character escapes are used to match a single character by its literal meaning.

The `\` character escape is used to match a single character by its literal meaning.

Examples:

            * `\\` matches a single backslash character.
            * `\.` matches a single period character.
            * `\*` matches a single asterisk character.
            * `\+` matches a single plus character.
            * `\?` matches a single question mark character.
            * `\^` matches a single caret character.



## Author

My name is Jerrod Linderman, I am a upcomming new web developer, I hope you learned something new. If you have any questions or comments please feel free to reach out to me on [Github](http://github.com/nvmax).
