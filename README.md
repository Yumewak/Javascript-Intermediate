# Javascript-Intermediate

## Adding event listeners to a button
```
Create a function that send an alert "I got clicked!" when the button gets click
and then select our button inside HTML and add the event listener that listen when ever get clicked.
```
```javascript
document.querySelector("button").addEventListener("click", function(){
    alert("I got clicked!")
})
```
```
Remember that an anonimous function doesn't have a name
```
```javascript
function () {
  alert("I got clicked");
} //This anonimous function can be passed to the listener like the example above
```
```
Challenge: add event listener to every single button
Hint: Take 5 lines or less
```
```javascript
for (let count = 0; count < document.querySelectorAll(".drum").length; count++) {
    document.querySelectorAll(".drum")[count].addEventListener("click", function(){
        alert("I got clicked!")
    })
}
```

## Higer order functions and passing functions as arguments
### Higer order functions
```
Higer order functions are functions that can take other functions as inputs
```
```
If you go to wikipedia javascript page and use "0$" to acces the "h1" element, you can modify
```
```javascript
$0.addEventListener("click", function() {
    console.log("I got clicked");
});
```
```
You can also specify it like this
```
```javascript
$0.addEventListener("click", respondToClick)
function respondToClick() {
    console.log("I got clicked");
}
```
```
The word click is the event that we're detecting and thats the input 1.
The second input is the function that should be called.
The first input specifying what event it should listent to.
The second input specifying what it should do once that event gets detected.
```
```
Challenge: Create a full set of operators for our calculator, add, multiply, divide, substract
the calculator function should be able to handle three inputs, the first two are numbers and
the thrid one are the operator.

Use the debugger of chrome:
debugger; // shift Enter
calculator (3, 4, multiply); // Enter
//Click the down arrow to step in to the next function call
```
```javascript
function add(num1, num2) {
    return num1 + num2;
}
 
function subtract(num1, num2) {
    return num1 - num2;
}
 
function multiply(num1, num2) {
    return num1 * num2;
}
 
function divide(num1, num2) {
    return num1 / num2;
}
 
function calculator(num1, num2, operator) {
    return operator(num1, num2);
}
```
