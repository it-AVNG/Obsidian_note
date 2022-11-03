# Adding script to Html
2ways of adding script to HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
    <title>Document</title>
</head>
<body>

<!-- arbitrary code here-->


<!--Java script initialized should put at the bottom of body-->
    <!-- Javascript initialize internally -->
    <script>
        console.log("Hello, world!")
        console.log("23 + 97");
        
    </script>
 <!-- or take script from a .js file -->
    <script src="numberTask.js"></script> <!--link the javascript file you want to run-->    
</body>
</html>

```


# Variables
A _variable_ is a "named storage" for data. `let` keyword help us to create a variable
```javascript
let message
```

Now we can put data to the variable called "message" using assigment operator `=` 

```javascript
let message

message = 'Hello'; //store the string Hello
alert(message); //shows the variable content
```

combination is also possible like such:

```javascript
let message = 'Hello'; // define the variable and assign the value

alert(message); //shows the variable content
```

variable can be declared in multiple of ways:
```javascript
let user = 'John', age = 25, message = 'Hello';

//or, recommended way

let user = 'John'; 
let age = 25; 
let message = 'Hello';

//or

let user = 'John', 
	age = 25, 
	message = 'Hello';
```

> if we want to create a variable with global (or function-level) accessibility (like in C/C++/Python), no block scope, assessible and retained its value through out the level, use `var` 
> `let` only at block leve, which means as soon as you are done with the variable, it clears it self.

## variable naming rule:
1. The name must contain only letters, digits, or the symbol $ and the under score `__`
2. First character is not a digit.
3. When the name contains Multiple words, camelCase is used
4. Case matters, `apple` and `APPLE` are 2 different variable.
5. best practice is use latin letters
6. refer to [reserved name](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords) as to not nameing the variable this way.
7. **ALWAYS** assign variables using either `let` `var` or `const` 
8. _Constant_ value are type in case letter and with underscore instead of camelCase style
9. the variable name should be clean and obvious, describing the data it is storing.
10. The variable should be human-readable like `userName` or `shoppingCart` .
11. Seldomly use short abbriviation like a, b, c
12. The name should be descriptive, not just general. Variable such as `houseData` is beter than just `data`
13. Agree with team and document of the Appendix before naming the variable for general definition.
14. Don't reuse the variable.
15. `const` variable means the value means it won't change through out the code as soon as it is assigned.

# Numbers:
Javascript arthimetic Operators 
+ `+` addition
+ `-` subtraction
+ `*` multiplicaton
+ `**` exponentiation (raise the number by the power of the operand)
+ `/` division
+ `%` modulus (remainder)
+ `++` increment
+ `--` decrement

Arithmetic operations: Basic math apply.
Operators list [full list is important]([JavaScript Operator Precedence (w3schools.com)](https://www.w3schools.com/js/js_precedence.asp))

Javascript number are *ALWAYS* 64-bit floating point.
![[Pasted image 20221030220449.png]]

Integers (numbers without a period or exponent notation) are accurate up to 15 digits.The maximum number of decimals is 17.Floating point arithmetic is not always 100% accurate. 

Some terminology to take note of: 
+ Operand - operators applied to. sometime they are called arguments instead.
+ Unary - single operand operator. like -1 or +3; 
+ An operator is _binary_ if it has two operands. 

Exponentiation also applied for non-integer number as well; like 1/2 and 3/4
Operator `+` can be used for string concatenation. When one operand is a `string` type in binary operation, the operation becomes string concatenate. 

In the case of non-binary operation, the mathematical operator precedence is applied. If a `string ` variable is called first, the operation becomes string concatenate. Else, the operation will convert to string concatenate when the `string` type operand is called.

*ONLY `+` can be use this way, others operators will convert the string into number for operating*

We can take advantage of the above propeties by adding operators (`+` included) into the variable called as a unary case to 'convert' them from being a string type into number type as shown in the below example 

```javascript
let apples = "2";
let oranges = "3";

// both values converted to numbers before the binary plus
alert( +apples + +oranges ); // 5

// the longer variant
// alert( Number(apples) + Number(oranges) ); // 5
```

## modify-inplace for operators:
`+=` and `*=` is a shorten operators that we can take advantage of.

## Bitwise operators [MDN Source]([Expressions and operators - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#bitwise_operators))
+ AND (&)
+ OR (|)
+ XOR (|)
+ NOT (~)
+ LEFTSHIFT (<<) Shifts `a` in binary representation `b` bits to the left, shifting in zeros from the right.
+ RIGHTSHIFT(>>) Shifts `a` in binary representation `b` bits to the right, discarding bits shifted off.
+ ZERO-FILL RIGHTSHIFT (>>>) Shifts `a` in binary representation `b` bits to the right, discarding bits shifted off, and shifting in zeros from the left.

the comma `,` is also an operator, rarely use but help with shorter code writing. the comma allows us to evaluate several expressions, dividing them with comma but the only result of the last one is returned. the comma has lower precedence than the `=`

we usually use them for quick use operation for example as the below code is giventh

```javascript
// three operations in one line
for (a = 1, b = 3, c = a * b; a < 10; a++) {
 ...
}
// the code above calculate quick the variable c and discard the rest, 
// reuse a for increment of the loop and keep b but dont return it in c;
```


# Strings:
it is a piece of text, really. a *method* is a bit of functionality that is built into the languague or into specific data type. 

just like a number, we can define a string like a variable, just put it into a quote bracket, either single quote or double quote is fine, but be consistant.

```javascript
const string = " The revolution will not be televised. ";
console.log(string);
```

### Escaping string Character
'Escaping' means we made it so that the characters are reconized as text. usually, we putting `\` before the character like so: 

```javascript
const bigmouth = 'I\'ve got no right to take my place…';
console.log(bigmouth);
```

Look at [escape sequence](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#escape_sequences) for more information. 

### Concatenate String
to join together string in Javascript, we can use a special template called _template literal_, it is anormal string, but using back tick ( \` ) 

It can works like normal strings, except we can include variables in it, wrapped inside `${}` characters and the variable value will be inserted to the result. 

```javascript
const name = "Chris";
const greeting = `Hello, ${name}`;
console.log(greeting); // "Hello, Chris"
```

the above code will return `greeting` variable value as `hello. Christ`. The same technique can be use to fuse 2 string variable together.

```javascript
const one =`Hello`;
const two =`Good day`;
const joined = `${one} ${two}`;
console.log(joined);
```

The above code will return the value `Hello Good day`.
In actual use case it should be similar to below code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
    <title>Document</title>
</head>
<body>
    <!-- Javascript initialize -->
    <button>Hit Me</button>

 <script src="stringTask.js"></script> 
</body>

</html>
```

and in stringTask.js
```javascript
const button = document.querySelector("button");

function greet() {
  const name = prompt("What is your name?");
  alert(`Hello ${name}, nice to see you!`);
}

button.addEventListener("click", greet);
```

The code utilise the `promt`, a short hand for `window.promt(..)` function, ask the user for input via popup diaglog box the stores the texxt they enter inside a give variable. Then use `alert` function to display the popup string which insert the input to a string variable.

We can also use `+` operators as a concatenate tool. as show above. Here is an example for using the `+` operator:

```javascript
const greeting = "Hello";
const name = "Chris";
console.log(greeting + ", " + name); // "Hello, Chris"
```

_note_: template literals have more readability.

### Numbers vs Strings
When concatenate 2 type of variables like strings and number, javascript makes more senes to turn number into strings rather than turning strings into number.
If you have a numeric variable that you want to convert to a string but not change otherwise, or a string variable that you want to convert to a number but not change otherwise, you can use the following two constructs:

number()
```javascript
const myString = "123";
const myNum = Number(myString);
console.log(typeof myNum);

```

toString()
```javascript
const myNum2 = 123;
const myString2 = myNum2.toString();
console.log(typeof myString2);
```

use case for these like a user enter a number in a text field which returns as strings. 

### Including expressions instrings
Template literals can helps us addexpression as well as simple variables and the results will include in the return result.

```javascript
const song = "Fight the Youth";
const score = 9;
const highestScore = 10;
const output = `I like the song ${song}. I gave it a score of ${
  (score / highestScore) * 100
}%.`;
console.log(output); // "I like the song Fight the Youth. I gave it a score of 90%."
```

Template literals also respect the added line break sho you can have the following code without any escaping character REGEX

```Javascript
const output = `I like the song.
I gave it a score of 90%.`;
console.log(output);

/*
I like the song.
I gave it a score of 90%.
*/

/*alternatively*/
const output = "I like the song.\nI gave it a score of 90%.";
console.log(output);

```
### Accessing Character in Strings
we can use either `charAt()` or treating the string as an array-type object.

```javascript
'cat'.charAt(1) // gives value "a"
```

or `'cat'[1]` gives the same value. but this methos does not support delete or assign value to these properties.

### Comparing Strings
