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
