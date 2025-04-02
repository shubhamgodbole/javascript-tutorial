## What is javascript & why it is use?
- Javascript is clinet side scripting language run on browser.
- **HTML** is used to define the structure of webpage
  - Header
  - Footer
  - Sidebar 
- **CSS** is used to styling the webpage
  - Text color
  - Background color
  - Alignment
  - Highlighting
- **Javascript** is used to perfom action on element of webpage
  - Click
  - Hover
 
## Let, Var, Const
- Let & Const are scoped variables
- Var is unscoped/global variable
- var keyword was used before 2015
- let and const keywords were added to JavaScript in 2015 ES6 version.
- Always use **const** if the value should not be changed
- Always use **const** if the type should not be changed (Arrays and Objects)
- Only use **let** if you can't use **const**
- Only use **var** if you MUST support old browsers.
- A variable declared without a value will have the value **undefined**
- If you re-declare a JavaScript variable declared with **var**, it will not lose its value.
  ```
    var a = 1;
    var a;
  ```
- You cannot re-declare a variable declared with **let** or **const**
- Const variable must be declare with its value
  ```
    Correct
    > const a = 3;
  ```
  ```
    Incorrect
    const a;
    a = 3;
    Error : SyntaxError: Missing initializer in const declaration
  ```
- Javascript variables can be declare with **$**
  ```
    let $ = "Hello World";
    let $$$ = 2;
    let $a = 5;
    let $1 = 5;
  ```

## Difference Between var, let and const

|        | Scope | Redeclare | Reassign | Hoisted | Binds this |
|--------|-------|-----------|----------|---------|------------|
| var    | No    | Yes       | Yes      | Yes     | Yes        |
| let    | Yes   | No        | Yes      | No      | No         |
| const  | Yes   | No        | No       | No      | No         |

**What is Good?**
- let and const have block scope.
- let and const can not be redeclared.
- let and const must be declared before use.
- let and const does not bind to this.
- let and const are not hoisted.

**What is Not Good?**
- var does not have to be declared.
- var is hoisted.
- var binds to this.

# Hoisting 
- It is an techniq to used variable before declaration
- Variables defined with **var** are hoisted to the top and can be initialized at any time.
  ```
     a = 10;
     var a;
  ```
- **why var is hoisted**
  - Its default behavior of javascript moving all declarations to the top of the current scope during the compilation
 
# this keyword
- Its uesd to access the property of object
  ```
    const person = {
      firstName: "John",
      lastName: "Doe",
      id: 5566,
      fullName: function() {
        return this.firstName + " " + this.lastName;
      }
    };
  ```
# Constructor
```
  function Person(first, last, age, eye) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eye;
  }

  const myFather = new Person("John", "Doe", 50, "blue");
  const myMother = new Person("Sally", "Rally", 48, "green");
  const mySister = new Person("Anna", "Rally", 18, "green");
  const mySelf = new Person("Johnny", "Rally", 22, "green");
```
