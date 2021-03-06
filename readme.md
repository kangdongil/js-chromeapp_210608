## ToDoList

- [x] Login
- [x] Remember Information
- [x] Clock
- [x] GeoLocation
- [x] Background
- [x] Random Quote
- [x] To-Do List

# 1.2 Requirements 이론 살펴보기

- HTML
  - <head>, <body>
  - <form>, <input>, <button>
- CSS
  - class vs. id
  - selector

# 1.3 Requirements 설치하기

- Browser: Chrome
- Text-Editor: VSCode
- Online IDE: replit

# 1.4 JavaScript란,

- Only Programming Language for FrontEnd
- JS is already bundled in Browser
- JS handles and modifies HTML Element

# 1.5 JavaScript Framework 알아보기

- React Native
  : Help create Android, iOS Application
- Electron JS
  : Help create Desktop App
- NodeJS
  : Create Backend with JS
- Socket.io
  : Configure Realtime Feature
- ml5.js
  : MachineLearning

# 2.0 Javascript 다루기

- Open Browser Console
  - `Ctrl+Shift+I`: Inspection Tool
- Connect CSS, JavaScript to HTML
  1. HTML: `!`
  2. `link:css` in <head>
  <link rel="stylesheet" href="style.css">
  3. `script:src` in end of <body>
  <script src="app.js"></script>
- Code Top to Bottom
- How to check value
  - `console.log();` to check value on console
  - `alert();`: show something with alert message
- if certain string used repeatly, use VARIABLE
  - VARIABLE should be uppercase
- if similar line of code used repeatly, use function
- To comment, start with `//`

# 2.1 데이터 타입(Data Type) 알아보기

- NUMERIC
  - integer
    `2, 11, 31`
  - float
    `1.5, 3.1`
- STRING(=TEXT)
  - cover value with "" or ''
    `"hello"`
  - number can be string, `"2"`
- BOOLEAN
  true or false
- OTHERS:
  - null: empty state
  - undefined: variable exist but value is not assigned
    `let [NAME];`
  - NaN: Not a Number
-

- typeof [VARIABLE]
  : check datatype of variable
- parseInt()
  : convert into integer
  if is not int, result is NaN.
- String()
  : convert into string
- isNaN()

# 2.2 Variable 알아보기

- Variable: Save or Hold Value
- Variable Naming Convention is `camelCase`
  - instead of space, UPPERCASE first letter
- always `const`, something `let`, never `var`

- const
  : hold constant value
  `const [NAME] = [VALUE];`
- let
  : allow updating value
  - Declare Variable
    `let [NAME] = [VALUE];`
  - Modify Variable
    `[NAME] = [NEW_VALUE];`
- var
  : old version of variable
  - can be redeclared, update avaliable

* How to use variable in string:
  1. by +
  2. ${VARIABLE} + ``(backtick)

# 2.5 Arrays, Objects 알아보기

- Arrays
  : lists of data using `[]`
  - Declare Arrays
    `const [NAME] = [items, items, ...];`
  - Get Items
    `NAME[seq]`
    - seq start from 0
  - Add Items on the end
    `[ARRAYS_NAME].push([ITEM]);`
- Objects
  : stores keyed data
  - Declare Object
    ```
    const [NAME] = {
        [PROP]: [VAL],
        [PROP]: [VAL], ...
    }
    ```
  - Use Object
    `[OBJECT].[PROPERTY]`
    `OBJECT["PROP"]`
    - can update or add value using object
      `player.name = ~;`
      `player.points = player.points + 15;`
  - Get Object's Property
    - `[OBJECT].length`

* JSON.stringify()
  : convert array into string
* JSON.parse()
  : convert string into array
* [ARRAY].forEach([FUNCTION])
  Execute function on each array's item
* [ARRAY].filter([FUNCTION])
  - return new array of filtered data
  - critera for filter is boolean(true or false)
  - if true then include, if false then exclude

# 2.7 Function 알아보기

- Function
  : Piece of reusable code
- Declare Function
  ```
  function [NAME]([ARG]) {
      ~
  }
  ```
- Execute Function
  `[FUNCTION]([ARG]);`
- Get data with 'Argument'
- Return Result from Function
  `return ~;`
  - after `return`, code doesn't work

* Function inside of Object
  - How to Create
    ```
    const [OBJ_NAME] = {
        [FUNC_NAME]: function([ARG]) {
            ~
        },
        ~
    }
    ```
  - How to Use
    `[OBJ].[FUNC]([ARG])`
* Arrow Function
  : can express function on shorter way
  `([ARG]) => Code`

# 2.13 조건문(Conditionals) 알아보기

- Conditionals: check if statement is true or not

  - if statement
    ```
    if (conition) {
      // condition == true
    }
    ```
  - if/else statement
    ```
    if (condition) {
      // condition == true
    } else {
      //condition == false
    }
    ```
  - else if

  * &&: AND Operator
  * ||: OR Operator
  * ===: Equal Operator
  * !==: Not Equal Operator

* condition: determine true or false, it should be boolean

# 3.0 JavaScript로 HTML Element 불러오기

- `document` Object: representation of HTML for JS
  `document.~`
  - Get HTML Element(getElementBy)
    - `document.getElementById("[ID]")`
    - `document.getElementByClassName("[className]")`
    - `document.getElementByTagName("[tagName]")`
  - Get HTML Element(QuerySelector)
    - `document.querySelector("~")`
      - querySelector works like CSS selector
      - for class, `.[CLASS]`
      - for id, `#[ID]`
      - querySelector only bring first element
    - `document.querySelectorAll("~")`
      - return a list of elements
  - Modify HTML Element
    - `[ELEMENT].innerText`
      : change text content
    - `[ELEMENT].style`
      : change css style

* Two Way to get child Element
  - Declare Parent Element and based on it
  - Start from document and express parent as CSS way

# 3.3 Events 다루기

- `[ELEMENT].addEventListener("[EVENT]", [FUNC]);`
  1. Set Element by `querySelector`
  2. Listen Event by `addEventListener`
  3. Execute Function
  - To get event's information, add first argument `event` to `addEventListener`
- `[ELEMENT].on[EVENT] = [FUNCTION];`
-

* MouseEvent
  - click
  - mouseenter
  - mouseleave
* Event(Window)
  - `window` Object: handle window screen
  - resize
  - CLIPBOARD
    - copy
    - cut
    - paste
  - CONNECTION
    - offline
    - online
* SubmitEvent
  - submit

# 3.8 ClassName으로 CSS 다루기

- [ELEMENT].className
  - substitute classname
  - replacement occur
- [ELEMENT].classList
  - classList.add([CLASSNAME])
    - preserve original one and add classname
  - classList.remove([CLASSNAME])
  - classList.toggle([CLASSNAME])
    - check classname exist and do the opposite

# 4.0 Login 구현하기

- Get User's Name
  1. Create <form> & <input>
  - disable form's default action(ex. refresh)
    `event.preventDefault();`
  2. Get <input> Value in VARIABLE
  3. Display Value
  - configure hidden with CSS
    `display: none;`
    - add or remove class "hidden" from classList
- Save User's Name
  - setItem `username` in localStorage
  - innerText `username`
- Load User's Name
  - if localStorage key `username` is null,
    - display <form>
    - addEventListener "submit"
  - if localStorage key `username` has value,
    - display <h1>
    - getItem `username` from localStorage

* local storage: save data on browser
  - [Inspector]-[Application]-[Storage]-[Local_Storage]
  - `localStorage.setItem([KEY], [VALUE]);`
  - `localStorage.getItem([KEY])`
  - `localStorage.removeItem([KEY])`

# 5.0 Clock 구현하기

- Interval and Timeouts
  - Function execute repeatly with interval
    `setInterval([FUNCTION], ~ms)`
  - Function execute once with delay
    `setTimeout([FUNCTION], ~ms)`
- Date Object
  - Get current Date Object
    `new Date()`
  - Get specific data from Date Object
    - `[DATE].getFullYear`
    - `[DATE].getMonth`
    - `[DATE].getDate`
    - `[DATE].getDay`
    - `[DATE].getHours`
    - `[DATE].getMinutes`
    - `[DATE].getSeconds`
- Configure Date Format with `padStart`
  - Pad in front of string when length is shorter
    `[STRING].padStart([LENGTH], [FILL])`
  - Pad back of string when length is shorter
    `[STRING].padEnd([LENGTH], [FILL])`

* 1000 ms(milisecond) = 1s(second)

# 6.0 Random Stuff 구현하기

- Random Float from 0 to 1
  - `Math.random()`
  - How to Extend random in certain value
    : Multiply total value(`* [TOTAL]`)
- Rounding
  - `Math.ceil()`
  - `Math.floor()`
  - `Math.round()`

# 6.1 JavaScript로 HTML Element 만들기

- `document.createElement();`
  - HTML Tag attribute is Element object's property
    `<img src="~"> = img.src`
- How to add Element to HTML
  - `[ELEMENT].appendChild();`
  - `[ELEMENT].prepend();`
  - `[ELEMENT].insertBefore([NEW], [REF]);`

# 7.0 ToDo 구현하기

- Create <form><ul><li> in HTML
- Declare const of HTML element in JS
- Create Input Form for ToDo
  - `event.preventDefault`
  - get the value from <input>
  - empty the value and `paintToDo`
- `paintToDo` function
  - get <input> value from argument
  - create <li> > <span>
  - innerText <span>
  - appendChild <li> in <ul>
- `deleteToDo` function
  - create <button>
  - addEventListener <button> "click"
  - `event.target.parentElement`
  - `[ELEMENT].remove`
- `saveToDo` function
  - Array: .push
    - instead of text, push object item
      which contain text and id
  - HTML: paintToDo
  - LocalStorage: saveToDos
  - if refresh, array = localstorage
    - make sure array is let variable
    - paint todo as `.forEach`

# 8.0 Weather 구현하기

- Get User's GeoLocation
  - get CurrentPosition
    `navigator.geolocation.getCurrentPosition([SUCCESS_FUNC], [ERROR_FUNC])`
  - get latitude and longitude
    `[OBJECT].coords.latitude`
    `[OBJECT].coords.longitude`
- Get weather from WeatherAPI
  ```
  fetch([URL])
  .then((response) => response.json())
  .then((data) => {~})
  ```

* [WeatherAPI](https://openweathermap.org/)
* API: help communicating between programs ad servers
  - simple command, do complicate things
