# CS | Regex Tutorial: Matching Hex Values

Regular Expressions, or Regex, are methods of validating specific instantances of common website elements that follow specific patters such as: Email structure, URL structure, HTML Tag structure, and so much more. Today I will be covering how we use regex to match up Hex / Color Values. 

## Summary

Hex Values are a specific 6 character code that represents a specific color. This is a perfect example where we can use a regex to look for the hex code pattern. I will be covering the components of the Hex Regex later in this document such as Anchors and Character Classes - first review the Hex Code Snipit below before you get started on the rest of this Gist. 

This is the Hex Code Regex code snipit.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

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

### Anchors:
We have to first identify these specific patterns, and we do that with Anchors. 

We use Anchers to find these patterns even while they are with in strings, the character `"^"` is the starting anchor while the `"$"` is the ending anchor.
- If you happen to need to have either character be included in thier starting or ending points, we will need to encompass the characters with a backslash. 

<br>
Example of how the starting and ending anchors display in the code:

- `"^Hello World, My name is Britt$"`

<br>
Here are examples of the ways how the anchor character behaves:

| Pattern    | Behaviour |
| -------- | ------- |
| ^A | "A" at the beginning of a line |
| A$ | "A" at the end of a line |
| A^ | "A^" anywhere on a line |
| $A | "$A" anywhere on a line |
| ^^ | "^" at the beginning of a line |
| $$ | "$" at the end of a line |

<br>

Finally, we need to apply the anchors to our specfic pattern that we are trying to identify. We will go more in detail in how to do so in the Quantifier Section.


### Quantifiers:
Quantifiers are used to quantify the number of times your regex should be repeated. By default they will try to find as many matches as possible however.

While there are many Quantifiers, we want to focus on the ones that are needed with Hex Codes. 
 - `*`, `?`, and `{}`
 

We do have a bit more of the structure to learn in this section as well. 
- While the `?` represents a true/false or a 1/0 booleen value, making that value or character to be optional. For our Hex Code Pattern, this allows the `#` to be optional in the pattern when the Quantifier searaches for it. 
  - `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
  - As the 3rd character, `?` is allowing the character in front of it to be optional. 

- Then the `{}` is searching for number of instances of the pattern string being found. We have two `{}` within the Hex Code Regex.
  - `[a-f0-9]{6}` & `[a-f0-9]{3}`

- Usin the first snip as an example, we can see that the code will want to find instances of 6 characters with in the bracket expression before it. Within the Bracket Expression, we can see that it will accept any charactes from a-f, and any interger from 0-9 up to 6 total characters within that string.


### Grouping Constructs:
Grouping allows us to treat a series of characters as a single variable.

With Grouping, we can encapsulate our characters away from the meta characters with the parenthese `()`. 
- `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
  - We only have 1 set of `()` and they are on the ends of the Hex Code Regex.


### Bracket Expressions:
The Bracket Expression is a part of the Regex that matches the unique pattern of the characters defined in the brackets: `[]`
- Hyphens will represent a range of characters that are accepted for the pattern. 
- I have touched a bit on the Brackets in the Quantifier Section, where the expression will allow up to 6 different characters but they have to be with in the limits set by the bracket expression.
  - `[a-f0-9]` 


### Character Classes
We use Character Classes as a way to define what is acceptable for a Character Set. 
- Character Sets are taking "many characters" = to be treated as "one variable" 
- Character sets noramlly live inside Bracket Expressions

Here are some examples of how Character Sets behave with in a Bracket Expression.

| Character Set | Behaviour |
| -------- | ------- |
| [] | The characters "[]" |
| [0] | The character "0" |
| [0-9] | Any number |
| [^0-9] | Any character other than a number |
| [^-0-9] | Any character except a number or a "-" |
| [0-9-z] | Any number,or any character between "9" and "z". |
  - `[a-f0-9]`, if we remove the brackets, we will get our Character Set: `a-f` & `0-9`
    - `a-f` = characters between a through f of the alphabet
    - `0-9` = characters between intergers from 0 through 9



### The OR Operator:
Not the Operating Room, the OR Operator allows us to choose between A OR B varialbes. We can expand to more than just 2 variables as well. 
- We use this symbol to show our OR Operator: `|`

For our Hex Codes, there is a single OR Operator smack dab in the middle of our Regex. 
- `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
- This Regex is saying to look for the patterns of a six {6} character hex value OR a three {3} character hex value. 

### Flags
Sometimes we need to search with more precision, Flags allow us to have advanced searching capabilities with in our regex.

Sometimes as we write the code, blocks of code could have inproper indentation or are purposefully placed on separate lines of code. The Flag allows, in our case, the Hex Code to be found. 
- The Anchors for the Hex Regex acts like a Flag as it protects the Regex from breaking while seemingly devided on different lines of code. 
- `^#?([a-f0-9]{6}|[a-f0-9]{3})$`


### Character Escapes
No Print Characters, or more commonly known as Character Escapes. There are a ton of different Character Escapes, but we will focus only on what the Hex Code Regex needs. 

We use the backslash `\\` 

- `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

## References
- Regular Expressions @grymoire [Click Here.](https://www.grymoire.com/Unix/Regular.html#:~:text=There%20are%20also%20two%20types,a%20feature%20in%20both%20types.)
- Regular Expressions @mdn web docs [Click Here.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Cheatsheet#groups_and_backreferences)
- How to Validate Hex Color Code @geeksforgeeks [Click Here.](https://www.geeksforgeeks.org/how-to-validate-hexadecimal-color-code-using-regular-expression/#)
- How Do Regular Expression Quantifier Work? @RobertElder [Click Here.](https://blog.robertelder.org/regular-expression-quantifiers/#:~:text=Quantifiers%20are%20used%20to%20quantify,times%20it%20should%20be%20repeated.)


## About The Author

My name is Brittany Jungclaus and I am currently studying at the U of Minnesota to become a Full Stack Web Developer. I want to be able to explore and build in a new space - the internet! I love learning about the specific perspective of the Developer in seeing the structure of how web pages display, databases in how they organize data, and how I can make an impact on the internet to use my new found skills to make my own space, tools, and data.

My Github has a lot of examples of my work, follow the link below and check it out! 

GitHub Profile: [Click Here.](https://github.com/NovaLanceBrittany)