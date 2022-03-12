# Regex Tutorial

# Introduction
This Regex tutorial is to help new users understand and define the sequence of special characters to verify a search term. 

A Regex can be defined as a specific search pattern. When a regex is included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string.

They also can be used to find and replace a character or sequence of characters within a string. They are also used to validate input data.

# Summary
This tutorial will serve as a break down of components of a regular expression used to match specific Hex Values. 

Hex values are commonly used in coding for color, using the hexadecimal color code format. 

On the web we can use hex triplet (hex color code) to represent colors on a web page. 

There are two formats, a standard hex triplet and a shorthand hex format, where both formats start with a #.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/


# Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

# Anchors
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

The first component that we will be breaking down are the anchors. As shown in the highlighted portion of our regular expression, the components that are highlighted are what we call anchors. A simple way one can remember Anchors is that they are used at the start and end of a string or expression. Similar to an actual anchor, being the start and end to a boats movement. In this specific case /^ and $/ signify the beginning or end of our expression.

# Quantifiers
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Quantifiers communicate the number of how many characters there are. Quantifiers specify how many number of times a group, character, or character class must be present in the input for a specific match to be found. By default, quantifiers are unforgivingly specific. Quantifiers will match as many characters as possible. If ",+,?,{}" characters are found within regular expressions, they fall under quantifiers. 

The question mark (?) indicates the expression will match 0 or 1 time. There are 2 types of formats we'll use the or operator to distinguish which format we are using. In our Hex Value regular expression we have {6} (Hex Triplet Format) and {3} (Shorthand Hex Format), this represents the length of the given component preceding these quantifiers. They should be 6 for {6} and 3 for {3}.

Hex Triplet Formats Include: #000000, #FFFFFFF, #0099CC. Shorthand Hex Format: #000, #FFF, #09C (the hex triplet format would just double each character: #09C -> #0099CC)

# OR Operator
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

The 'or' operator within a regular expression is defined using the '|' element. The 'or' operator indicates that it could be either of the components that we are separating with the |. 

For our hex value regular expression we have ([a-f0-9]{6}|[a-f0-9]{3}). Bare in mind, the 'or' operator separates these 2 components. This means that our hex value could be anywhere from 3 characters [a-f0-9]{3} to 6 characters [a-f0-9]{6}.

# Character Classes
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Character classes are important because they're components within our regular expressions that tell us what characters to expect. For example above, our character classes are confined within brackets []. For our example we have 2 character classes: [a-f0-9] and [a-f0-9] which searches for the same values. 

We break down what the characters are searching for within these character classes. a-f searches for letters a-f and 0-9 searches for digits 0-9.

# Bracket Expressions
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Bracket expressions in our regular expression represents the introduction of a character class or quantifier statement. In our example we use parenthesis to define our bracket expressions. Please review the example above.

# Greedy and Lazy Match
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

To better understand, we need to compare Greedy and Lazy matches. A greedy match tries to match an element as often as possible. Where in retrospect, a lazy match tries to match an element as little as possible. When reviewing our example above, we have ? which signifies lazy quantifier. This is referred to a lazy quantifier because it causes the regular expression engine to match as few occurances as possible. We can simply turn this lazy match into a greedy one by adding a ?.

# Author

All contents here are allowed to be used for general/ public consumption. The following link is to the authors github profile. https://github.com/michaelcmaresco

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

GitHub: michaelcmaresco