# JavaScript Essential Training
[Link to Class](https://www.lynda.com/JavaScript-tutorials/JavaScript-Essential-Training/574716-2.html)

#### Inline JavaScript
If we want the `<script>` to run _before_ the contents of the page have rendered, add it to the `<head>`.

If we want the `<script>` to run _after_ the contents of the page have rendered, add it after the `</body>`.

"JavaScript gets rendered as soon as the browser gets ahold of it.
That means the order in which you provide your content and your JavaScript, is the order your browser will render it in."

---
#### JavaScript Render Blocking

Anytime a browser encounters a JavaScript file reference, it stops the rendering until the script file is downloaded and executed

---

### JavaScript Loading Methods:

| Right Away Loading |
| ------------------ |
| ![JS Right Away Loading](https://i.imgur.com/UV7FqxB.png) |

| Asynchronous Loading |
| -------------------- |
| ![JS Asynchronous Loading](https://i.imgur.com/ezxq1rO.png) |

| Deferred Loading |
| ---------------- |
| ![JS Deferred Loading](https://i.imgur.com/4wuzdCt.png) |

---

### JS Coding Conventions

* JS is case sensitive. Camel Case bing the preferred method

* Whitespace matters (to humans). Add whitespace to make your code more readable

* End each statement with a semicolon. Helps make code more readable and easy to understand when a statement is finished.

* Use comments liberally. Helps provide context for self and future develops.

---

## Data

### Variables

Defined with ``` var a = 'a'; ```

You cannot create a variable that begins with a number, but it can include them in the name.

```
var a = 4;
var b = 5;
var sum = a + b;
```

"To avoid global scope, always declare your variables"

---
### Data Types
You can find the data type of a variable with this function
```
console.log(typeof variableName);
```

#### Numeric Data
Stores regular numbers and integers
```
var number      = 1;
var integer     = 3.141592;
var negNumber   = -1;
var negInteger  = -3.141592;
```

#### String Data
Stores strings of letters and symbols
```
var string      = "Strings are typically words and sentences.";
var mixedQuote  = 'This keeps the "quotation" marks.';
var escQuotes   = "Quotes can also be \"escaped\".";
```

#### Boolean Data
Stores one or the other of the binary pair true/false
```
var theSunIsWarm          = true;
var theMoonIsMadeOfCheese = false;
```

#### null data
Stores the intentional absence of a value
```
var emptyInside = null;
```

#### undefined Data
Placeholder when a variable is not set
```
var justAnotherVariable;
// This variable is undefined
```
---

### Operators
Assignment Operator: `=`

The equals symbol assigns a value to a variable.

#### Arithmetic Operators

| `+` | `-` | `*` | `/` | `<` | `>` |
|----------|-------------|----------------|----------|-----------|--------------|
| Addition | Subtraction | Multiplication | Division | Less Than | Greater Than |

#### Shorthand Operators

| `+=` | `-=` | `*=` | `/=` | `>=` | `<=` |
|-------------|--------------|--------------|-----------------|-----------------------|--------------------------|
| Plus Equals | Minus Equals | Times Equals | Division Equals | Less Than or Equal to | Greater Than or Equal to |

| `==` | `===` | `!=` | `!==` |
|----------|-----------------|--------------|----------------------|
| Equal to | Strict Equal to | Not Equal to | Not Strict Equals to |

#### Unary Operators

| `++` | `--` |
|-----------|-------------|
| Plus Plus | Minus Minus |

**NaN** will appear when one or more data types being operated on is a string.

---

### Conditionals and Logic

```
if ( some condition ) {
  Do something.
}
```

If `a` is equal to (contains the same value as) `b`:
```
if ( a == b ) {
  Do something.
} else {
  Do something else.
}
```

Example:
```
var a = 5;
var b = 5;
var theNumbersMatch;
if ( a == b ) {
  theNumbersMatch = true;
} else {
  theNumbersMatch = false;
}

console.log("The numbers match: " + theNumbersMatch);
```
Output: `The numbers match: True`

#### Logical Operators

| `&&` | `\|\|` |
|:---:|:---:|
| And | Or |
| `if ( a == b && c == d ) { }` | `if ( a == b \|\| c == d ) { }` |
| If `a` equals `b` **AND** `c` equals `d` | If `a` equals `b` **OR** `c` equals `d` |

---

### Array

A container to store multiple values which do not have to conform to a single type. They are indexed and indexing starts at 0.

#### Array Properties and Methods

**Property**: Meta information about the object

**Method**: Function that belongs to the object

[Full List of Methods](https://www.w3schools.com/jsref/jsref_obj_array.asp)

---

### Functions

There are 3 types of functions:
- **Named functions**
Executed when called by name.

- **Anonymous functions**
Executed once triggered.

- **Immediately invoked function expressions**
These run the moment the browser encounters them.

#### Function Structure

##### Named Functions

```
function multiply(a,b) {
  var result = a * b;
  console.log(result);
  return result;
}

var multiplied = multiply(3,4);
```

- We define the function with the keyword `function`
- Then provide a name for our function (if it is a named function and not anonymous)
- Parenthesis follow the name of the function and this is called the 'Arguments Object' and is where we include our expectations for data
- This is followed by a pair of curly braces which will enclose our code block
- The desired logic is then added to the code block
- We conclude by calling the named function and provided it with data

##### Anonymous Functions

Anonymous functions don't have a name, so the parenthesis appears right after `function`.

```
var divided = function() {
  var result = 3 / 4;
  console.log("3 divided by 4 is ", result);
}
divided();
```

##### Immediately Invoked Function Expressions

Anonymous functions with another parenthesis pair at the end to trigger them; all wrapped inside parenthesis.

```
(function() {
  var result = 12 / 0.75;
  console.log("12 divided by 0.75 is ", result);
  }())
```

---

Functions can return values to where they were called from using the `return` keyword.
Whatever is returned is not executed directly, but instead captured in a variable or used immediately in another function.

---

####
