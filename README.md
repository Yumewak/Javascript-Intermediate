# Javascript-Intermediate

## Adding Javascript to websites
```html
//Inline Javascript
<body onload="alert('Hello')">

//Internal Javascript
    <script type="text/javascript">
        alert(`"Hello"`);
    </script>
  
//External Javascript
<script src="./index.js"></script>
  //index.js
  alert("hello");
```

## Introduction to the Document Object Model
```html
<html lang="en">
<head>
    <title>My Website</title>
</head>
<body>
    <button>Alert</button>
</body>
</html>
```
![Sin título](https://user-images.githubusercontent.com/93165649/151464612-50654f1c-b890-40e7-b668-1660722239ef.png)
![16g5gfert](https://user-images.githubusercontent.com/93165649/151465209-5f24c04d-e73c-478b-bff2-8fe82563d382.png)
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My Website</title>
    <link rel="stylesheet" href="./styles.css">
</head>
<body>
    <h1>Hello </h1>

    <input type="checkbox">

    <button style=":active: color:red;">ClickMe</button>
    <ul>
        <li class="list">
            <a href="https://www.google.com">Google</a>
        </li>
        <li class="list">Second</li>
        <li class="list">Third</li>
    </ul>

    <script src="./index.js"></script>
</body>
</html>
```
```javascript
document.firstElementChild.lastElementChild.firstElementChild //This will select the "<h1>Hello</h1>" tag thats inside the body
var heading = document.firstElementChild.lastElementChild.firstElementChild // This will save it inside the variable "heading" the DOM line of code
heading.innerHTML = "Good Bye" // This modify the innerHTML of the heading
heading.style.color = "red" // Changes the text color of the element that is selected to red
document.querySelector("input").click() // This looks inside our entire document for the object that has the selector of "input" and call a method "click". click simulates a mouse click
```
```
The objects inside the DOM can have properties and methods
Properties: Describe something about the object
.innerHTML
.style
.firstChild

Methods: Are the things that the object can do
click()
appendChild()
setAttribute()

car.color; //get the value of the property         "Get Property
car.numberOfDoors = 0; // set the number of doors  "Set Property" 
car.drive (); // call the method drive             "Call Method"
```
```javascript
//Diferent ways of change a text
document.getElementsByTagName("li").item(2).innerHTML = "Mario"
document.getElementsByTagName("li")[2].innerHTML = "Ulrich"
document.querySelector("ul").lastElementChild.innerHTML = "Ashley"
```
