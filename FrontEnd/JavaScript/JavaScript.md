
## JavaScript Crush Course

### Data Types

Declarations: `const`, `let`, `var`,  **weak type checking**
```javascript
const constantVar = 42; // Unchangeable
var oldStyleVar = 17;   // Global scope

for(let blockVar = 0; blockVar < 10; blockVar++) {
    // Block scope
}
```

#### Primitive Types:
1. `Number`: integers, floats, `NaN`
2. `String`
3. `Boolean`: 
   - `true` <=> `!0`, non-empty string
   - `false` <=> `0`, `null`, `undefined`, `NaN`, empty string
4. `Undefined`: declared but not initialized
5. `Null`: explicitly empty
---
### Objects
#### JavaScript Objects:
1. `Array`: ordered list of values
   ```javascript
   let fruits = ["Apple", "Banana", "Cherry"];
   let numbers = new Array(1, 2, 3, 4, 5);
   ```
2. String: `String` object
   ```javascript
   let str = new String("Hello World");
   let str = "Hello World";
   ```
3. `Function`: reusable block of code
   ```javascript
   function add(a, b) {
     return a + b;
   }
   ```
4. `Object`: key-value pairs
   ```javascript
   let person = {
     name :  "Kevin",
     age  : 19
   };
   Console.log(Object.keys(person)); // ["name", "age"]
   Console.log(Object.values(person)); // ["Kevin", 19]
   ```
5. `Math`: used for mathematical operations
6. `RegExp`: Regular expressions, used for pattern matching

#### Browser Objects:
1. `Window`
   ```javascript
   window.alert("Popup Message");

   window.confirm("Yes or No?"); // `Yes` -> true, `No` -> false

   window.setTimeout(function() {
     alert("Function executed only once, with a delay of 3 seconds");
   }, 3000); 

   window.setInterval(function() {
     alert("Function executed every 3 seconds");
   }, 3000);
   ```
2. `History`
   ```javascript
   window.history.back(); // Go back to the previous page;
   window.history.forward(); // Go forward to the next page;
   ```
3. `Location`
   ```javascript
   location.href = "https://www.google.com"; // Redirect to Google
   ```
4. `Navigator`
5. `Screen`

#### DOM(Document Object Model)
`Element`: fetched the object then manipulated their attributes, events, and styles: 
  - `.src(newURL)`
  - `.href(newURL)`
  - `.innerHTML(NewContent)`
  - `.style.property = newStyle`
  - `.addEventListener(event, function)` 
   ```javascript
   document.getElementById("Id").innerHTML = "Changed Content";
   document.getElementByTagName("HTML tag, div, span, etc."); // -> Array of elements
   document.getElementByName("name attribute"); // -> Array of elements
   document.getElementByClassName("class attribute"); // -> Array of elements
  ```


---
### Output
```javascript
console.log("Hello World in browser's console");
window.alert("Hello World in a popup window");
document.write("Hello World in the HTML document");
```


### Events Listener
Bounding:
```javascript
<input type="button", onclick="on()" >
<input type="button", id="btn">

<script>
  function on() {
    alert("Button Clicked");
  }

   document.getElementById("btn").onclick = function() {
     alert("Button Clicked");
   }
</script>
```

Events:
- `onblur`: when an element loses focus
- `onfocus`: when an element gets focus
- `onchange`: when the content of an element changes
- `ondblclick`: when an element is double clicked
- `onkeydown`: when a key is pressed
- `onwheel`: when the mouse wheel rolls up or down over an element

