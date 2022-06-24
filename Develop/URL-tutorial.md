# Regex Tutorial

Reqex is a tool used by many developers around the world. It is very useful when incorporating aspects of user input in your websites that need to be in a correct format. By creating a regex expression, you can tell a user if their input is in the correct format that the host wants it to be in. An example of this would be a contact form for someone to reach back out to you, and they need your email address to contact you. If the input is accidently not an acceptable email address format the user should be issued a warning to fix their email.

## Summary

The regex expression that I will be describing to you today is the URL format. The format for a URL regex expression looks like this
 `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`
 I will explain to you what each of these symbols and letters mean in a regex expression, as well as how they fit for our example.

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
Regex components are the tools to which you can build your expression. Examples of these would be all the topics considered below. They could be seen as the building blocks to your expression.

### Anchors
Anchors are used to describe the position in your expression. You can use `^` to symbolize the start of your string or line, you can use `$` to descreibe the end of the string or line. A `\A` symbolizes the start of a string but not a line, and a `\Z` symbolizes the end of a string but not a line. In our URL example you can see the first character after the `\` is a `*` to symbolize the start of the string, as well as a `$` at the end to symbolize the end of the string.

### Quantifiers
Quantifies are used as the name might imply, to quantifiy how many times you want a character to be entered or how long for something to be. In our example we use quantifies in the middle section `{2,6}` to show that we need a .com or a .uk .org or some other ending to a url. So it has to be between 2 and 6 characters long because that is how long most or all of the endings to websites are. the `{}` are to symbolize the quantifiers. The `+` in the equation above is also a quantifier to symbolize to match 1 or more of the preceding expression. As we use it to match one or more of the `[\da-z\.-]` line.

### OR Operator
An OR operator is also pretty self explanatory. You would use `||` to describe if you want something or another thing. We do not use it in our expression above.

### Character Classes
A character class is used to describe letters or numbers, as well as special characters. Our example uses them in the `\da-z` section or the `a-z` describing either digits and letters or just letters. We need them there because in the first section you can have numbers in your website name but in the second instance where it is just `a-z` we need just letters because that is where our .com or .org would go and you cannot use numbers.

### Flags
A flag is a optional parameter to a regex that modifies its behavior for searching. We do not have any flags in our example.

### Grouping and Capturing
Grouping and capturing is a very important part of regex expressions. They are how you seperate what you want in your expression. To capture a group you would use `()`. In our example above we have three different groups to explain our website name, the .com , and anything else afterwards to describe a specific part of the website.

### Bracket Expressions
Bracket expressions are used to describe specific characters. An example of this would be `[0-9]` to match any character in that set range. We use them in the URL expression to show the range of digits or letters used to create the website name in the first set of brackets.

### Greedy and Lazy Match
A greedy match means your expression will match as large a group as possible, a lazy match means it will match the smallest group possible.

### Boundaries
Boundaries are used to separate groups. They are represented by `\b` and is not used in our expression above. You would use them if say you wanted letters on one side and numbers on another.

### Back-references
A back-reference identifies a previously matched group and looks for exactly the same text again. It is not in our expression but is displayed as `\b`

### Look-ahead and Look-behind
A look-ahead and a look-behind are pretty self explanatory. A look-behind means to check what is before your regex match and vice versa, a look-ahead means checking what is after your match. It is not necessary in our URL expression.

## Author

Hello, my name is Alejandro Restrepo and I am a full-stack developer student.
https://github.com/ARestrepo12