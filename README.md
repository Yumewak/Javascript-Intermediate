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

## Selecting HTML Elements with Javascript
```javascript
document.getElementsByTagName("li")[2].style.color = "purple" // It searches for the element with a particular tag name, the result is an array

document.getElementsByTagName("li").length // length property tell how many items are in the array

document.getElementsByClassName("btn")[0] // Returns an array of element with a particular class name

document.getElementById("title").innerHTML = "Good Bye" // Using this method you only get back one item instead of an array

document.querySelector("") // Only returns a single item, the string inside the parentheses is a selector
("body")
(".navbar")
("#title")
//With selectors we can combine different things, for example an id with a class, or a class with an element
document.querySelector("li a")
document.querySelector("li.item") // When you're combining selectors that occur in the same element there are no spaces

document.querySelectorAll("#list .item")[2] //Return an array with all of the objects that match that selector
```

## Manipulating and Changing Styles of HTML Elements with Javascript
```javascript
// Every singles CSS property can be changed in this way using Javascript, but the property names might look different
document.querySelector("h1").style.color = "red" 
//Javascript naming conventions tend to be camel cased, and the values have to be represented as strings
document.querySelector("h1").style.fontSize = "10rem"
```
[HTML DOM Style Object](https://www.w3schools.com/jsref/dom_obj_style.asp)

## The separation of concerns: Structure vs Style vs Behaviour
```javascript
//Class list
//The add method can use to add classes to the "classList"
document.querySelector("button").classList.add("invisible")
document.querySelector("button").classList.remove("invisible")
document.querySelector("button").classList.toggle("invisible")
```

## Text Manipulation and the Text Content Property
```javascript
// Gives you the HTML that's in between the element tags, you can also add HTML code on the fly
document.querySelector("h1").innerHTML = "<em>Good Bye</em>"
//Just show you the text
document.getElementById("title").textContent = "GoodBye"
```

## Manupulating HTML element attributes
```javascript
// Get the list of attributes
document.querySelector("a").attributes;
// Retrieve the current value of that attribute
document.querySelector("a").getAttribute("href")
// Change the attirbute
document.querySelector("a").setAttribute("href", "https://www.bing.com")
```
