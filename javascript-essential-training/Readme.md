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

|                   `&&`                   |                    `||`                 |
|------------------------------------------|-----------------------------------------|
|                   And                    |                     Or                  |
<!-- |       `if ( a == b && c == d ) { }`      |       `if ( a == b || c == d ) { }`     | -->
<!-- | If `a` equals `b` **AND** `c` equals `d` | If `a` equals `b` **OR** `c` equals `d` | -->
