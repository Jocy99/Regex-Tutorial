# Regular Expressions Tutorial 

A regex, short for regular expression, is a powerful and flexible tool used in programming to search, match, and manipulate strings of text based on specific patterns. Regex allows you to define patterns of characters and symbols to describe what constitutes a valid or matching string.
Today I will be explaining and breaking down a regular expression that will help us match a user's email.

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
Here is the expression component we will be disecting, which matches a user's  Email :
– /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors
The '^' caret anchor represents the start of a line or the email in this case. The '$' symbolizes the end of the input string. The '$' asserts that the matching pattern must occur at the end of the string.

### Quantifiers
There are two types of quantifiers used in our Regex. The '+' and the '{2,6}' help control how many times a particular character or group of characters should appear in the pattern we're trying to match. The plus quantifier means it must appear atleast once but can appear more than once. The Brace quantifier speficies the range.

### Grouping Constructs
In our expression example above, our grouping constructors serve two main purposes. Parenthesis are used to group characters together allowing us to apply quantifiers. Grouping constructors also help in defining scope of alteration using the '|'.

### Bracket Expressions
Bracket expressions(enclosed with square brackets) are used to define a set of characters that can match a single character in the text input. You can specify a list of characters or a range. 

### Character Classes
Character sets inside the bracket expression define a set of characters that can match a single character. Here's what each character within our expression mean:
    a-z: Matches any lowercase letter from 'a' to 'z'.
    0-9: Matches any digit from '0' to '9'.
    _: Matches an underscore character.
    \ .: Matches a literal dot character (the backslash \ is used to escape the dot because the dot has a special meaning in regular expressions).
So, this character class matches any lowercase letter, digit, underscore, or dot.

### The OR Operator
The '|' character in our expression represents the OR operator. You can also use parenthesis to group together different alternatives of the OR operator. In our regex the first group ([a-z0-9_\.-]+) matches the local part of the email address like the username. The second group ([\da-z\.-]+) matches the domain part of the email address. The last group ([a-z\.]{2,6}) matches the top-level domain (TLD) part, which could be something like ".com". We use the grouped alternatives to represent the structure of a valid email.

### Flags
Flags are typically added after the regular expression pattern, and they influence how the regular expressions matching is performed. (g) meaning global, (i) is a case sentitive flag and (m) modifies the behavior of '^' and '$' anchors allowing them to start and a line in a multiline input string.

### Character Escapes
Character escapes are used to represent certain characters or character classes. Here are the character escapes used in our regular expression: 
\d is a character escape representing any digit from 0 to 9. It's equivalent to the character class [0-9]. In this regex, it's used to match a digit in the domain part of an email address, such as "example123.com.".

`\.` (dot): The dot . is a metacharacter that usually matches any character except a newline. However, when it is preceded by a backslash `\.` as in `\.` in the regular expression, it matches a literal dot character. In this regex, `\.` is used to match the dot in the domain part of an email address and the dot in the top-level domain (TLD).

## Author
My name is Jocelyn, and with my passion for continuous learning, I've recently embarked on an exciting journey of mastering JavaScript, the dynamic programming language that powers the web.

As I delved deeper into the world of JavaScript, I encountered a fascinating and somewhat challenging aspect of it - regular expressions, also known as regex. These powerful tools for pattern matching and text manipulation intrigued me, and I was determined to conquer them.

Driven by my passion for learning and my ability to break down complex concepts into manageable pieces, I quickly grasped the fundamentals of JavaScript and became proficient in using regex. It didn't take long before I decided to combine my newfound skills with my love for teaching.

The result? A comprehensive regex tutorial on GitHub that I painstakingly crafted. My goal was simple: to make regex approachable for everyone by providing clear explanations, practical examples, and interactive exercises.

To my delight, the tutorial gained traction within the programming community. It was immensely rewarding to see my commitment to learning and my passion for teaching reflected in the positive feedback and engagement it received.
https://github.com/Jocy99/Regex-Tutorial

