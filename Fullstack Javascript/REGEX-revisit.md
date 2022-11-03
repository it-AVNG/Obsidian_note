Is use for validating strings and look up multiple strings that satisfy a certain condition.

# Simple REGEX pattern
For Example, let create a REGEX that look for a word, inthis case, 'ninja'

```Regex
/ninja
```

That is it! it just that simple. However notice the `/`, in Regex it is called _demiliters_ these are _boundaries_ of our regex. Depending on the *language* that we use the delimiter will change, google it if you forget. remember google is your friend.

The above expression only look for the _first_ value that it is returned then stop, which is not helpful really, we can modify this to *return ALL instances* the regex is met.

```Regex
/ninja/g
```

the `g` end of the regex  is called _flags_ flags are rules applied to regex for looking up the strings, in this case we are look for word 'ninja' in global scale, which returns multiple instances it met.
Regular expressions may have flags that affect the search.

# Flags

There are only 6 of them in JavaScript:

- `i` :With this flag the search is case-insensitive: no difference between A and a 
- `g` :With this flag the search looks for all matches, without it – only the first match is returned.
- `m` :Multiline mode 
- `s` :Enables “dotall” mode, that allows a dot . to match newline character `\n`  
- `u` :Enables full Unicode support. The flag enables correct processing of surrogate pairs.
- `y` :“Sticky” mode: searching at the exact position in the text 

# Character Sets

it is good and all, but RegEx power is in pattern matching, not exact words. _Introducing Characterset_, which is a way to match different characters in **the same position**.

For example, we are not only looking for a word 'ninja', we are looking for a group of word consist of 'inja' and at the begining and everything else is matched except for 'p' and 'e' character. a _character set_ is denoted with the square bracket `[]` and everything inside is considered as matched. and with `^pe` we exclude the characters

```Regex
/[^pe]inja/gi
```

The character '^' inside Regex is use for **except** case.

# Ranges

For if we want to match letters in a Range in an exact _position_ we modify our characterset as '[a-z]' : which means where letter in the position is match with appropriate flag.

for example, our `/[^pe]inja/`  is turned to `/[a-z]inja/`

# Metacharacters and special Character 

Are like short codes for common matching pattens, an additional to range of haracter. 
+ `\d` Any digits, short-code for [0-9]
+ `\D` Any non-digits, short-code for [^0-9]
+ `\s` Any white space character, short-code for [\t\n\x0B\f\r]
+ `\S` Any non-whitespace character
+ `\w` Any word character, short-code for [a-zA-Z_0-9]
+ `\W` Any non-word character
+ `\b` Represents a word boundary
+ `\B` Represents a non-word boundary
+ `\t` matching any tab characters

Special characters are behaviour that are special
+ `+` one ore more chaqualifiers
+ `\` escape character : make the character escape their usual function
+ `[]` charactersets
+ `[^]` negate symbol in the character set
+ `?` Zero-or-one quantifier
+ '.' Any-things-goes here except newline  characters
+ `*` 0-or-more quantifier
+ `{_number_}` the qntifier sets the number of characters that we are looking for in the pattern.

Quantifiers *+, \*, ? and {n}* is appended to a character or character sets or a [..] set, etc. 

# Starting and Endding patterns
Imagine we have a forms with a requirement that has 5 exact characters, there is numerousway to count 5 characters in a strings. We will include a starting and ending patterns called `^ ... $`

`^` means the Regex following willl be at the start
`$` means the preceding Regex should be at the End of the pattern
With the above combination, we said the Regex in the field must be exact. 

# Alternate Characters
`|` This means or, we can say `(R|T)aya` means we are looking for the Regex is looking for Raya or Taya. 

The `()` means telling the Regex to evaluate the internal a seperate entity for Regex regulation.

For example. We are looking for a combination of 'balls' that consist of basketball, volleyball, football. We could extend it to also include 'ball' inside by adding `?` modifier like above example

```Regex
/(basket|volley|foot)?ball/gi
```

# REGEX in javascript

```javascript
<!-- create a Regex variable matching all the words in the alphabet disregard case-->
var regex=/[a-z]/gi;

var regex= new Regexp(/[a-z]/,'gi');
```
