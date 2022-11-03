# Email Match - Regex Tutorial

/^([a-zA-Z0-9._%-]+)@([\da-zA-Z\.-]+)\.([a-zA-Z]{2,6})*$/ -- look confusing? this is a common email regex validator. 

## Summary

A REGEX is a series of characters used to describe a particular input pattern. In the case of our email pattern, the regex for email format validation contains characters that our server can use to verify that the email provided matches the proper format of an email address (your email name) @ (ex. yahoo,gmail) . (ext. 'com' 'gov' 'io' ...). Lets dive into the wierd characters and what they actually mean, then it will make a lot more sense!

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
This email validation expression uses two anchors. The first(starting)anchor is the `^`, the last(ending)anchor is the `$`.
### Quantifiers
Quantifiers specify the the amount of characters are allowed to be used for the match to be made. in our case the `+` is used two times here `[a-zA-Z0-9._%-]+` and here `[\da-zA-Z\.-]+`.
The `+` quantifier says that we can have any number of characters we want, but if we want to be more precise with the amount of characters we would use `[a-zA-Z0-9.-]{4,20}`. the `{4,20}` is where the `+` used to be. All this is saying is that instead of limitless characters, now we have to have at least 4 characters and no more that 20.
### OR Operator
In this example we do not use an OR Operator. an example of an or operator is `(t|T)` this will match either `t` or `T` from the input string.
### Character Classes
in our email example we are using the character class `\d` seen in [\da-zA-Z\.-]. this is shorthand for saying `[0,9]`.
### Flags
A flag is an optional parameter to a regex that modifies its behavior of searching. flags come after the ending `/` of a regex expression, they are optional but some examples are `i`, which ingnores letter casing. `m` is a multiline flag.
### Grouping and Capturing
in our expression the first group we have is `(your email name)` which appears as `/^([a-zA-Z0-9._%-]+)` then we have the `@` symbol.
Next we have the email domain `(ex. yahoo, gmail ...)` which appears as  `([\da-zA-Z\.-]+)`. last we have the extension `(ex. com, gov, io)` which appears as `([a-zA-Z]{2,6})*$/`
### Bracket Expressions
in our regex we use these bracket expressions [a-zA-Z0-9._%-], [\da-zA-Z\.-], and [a-zA-Z] . these allow for lower-case/uper-case/numbers 1-9 and some special characters.
### Greedy and Lazy Match
this REGEX uses Greedy match because of the `+` quantifier. Greedy match means this expression will match as large a group as possible (`+`).
### Boundaries
in this example we did not use boundaries,but i will show an example. a boundary will take place of our anchors and is more suited for a word search regex. `\bcat\b` in this example say in our page we have "cat, tomcat, catfish". this regex would only find cat because of the start and ending boundary syntax. However if we take away the end `\b` then we would find anywhere that the letters "cat" are found, whether by itself or inside of another word.
### Back-references
Backreferences refer to a previously captured group in the same regular expression.
### Look-ahead and Look-behind

## Author
My name is Brayden McMahan i am a current studen at UNCC's coding bootcamp! you can find me on github at https://github.com/banjosquash.

