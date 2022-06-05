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

## How to play sounds on a website
```
First create a new variable and then create new audio object, and specifies the name of the sound file
and then play the new object with the method "play()"
```
```javascript
var audio = new Audio('audio_file.mp3')
audio.play();
```
```
Refreshing memory about Introducction to the DOM
We know that we can grab the innerHTML and we can use that to differentiate the buttons so that when
a user press a button we get the character that the button contains and then we use that to determine
wich sound we're going to play.

this.
this Is basically the identity of the button that triggered the event listener
try console.log(this) and console.log(this.innerHTML)
```
```
Challege: Take a look  inside the styles.css and assing a background image to each of the buttons
```
```css
background-image: url("");
```
```
Challege: Modify the code to change the text color of the button that got clicked to the color white
```
```javascript
for (let count = 0; count < document.querySelectorAll(".drum").length; count++) {
    document.querySelectorAll(".drum")[count].addEventListener("click", function(){
        this.style.color = "white";
    })
}
```
[HTML Audio Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAudioElement) \
[HTML Media Elements - Methods](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement#methods) \
[How to play audio](https://stackoverflow.com/questions/9419263/how-to-play-audio)

## Javascript objects
### Object
```
Whe can see an object has an excel table
Properties   | bellBoy1             | bellBoy2 | bellBoy3
--------------------------------------------
name         |timmy                 |
age          |19                    |
hasWorkPermit|true                  |
languages    |["french", "englis"]  |
```
```javascript
//Creating an object manually
var bellBoy1 = {
    name: "Timmy",
    age : 19,
    hasWorkPermit: true,
    languages:["French", "English"]
}

//We we're using the dot to acces the property "name"
alert("Hello, my name is" + bellBoy1.name) // Hello, my name is timmy

//When we're creating properties inside objects we're just creating a variable that's associated with another variable
//And you can assign it any value you wish, number, string, array, etc.
```
```
Constructor Function also know Object "Factory"
```
```javascript
function BellyBoy(name, age, hasWorkPermit, languages) { // The name of the constructor function have to be capitalized, no camelcase
    this.name = name;
    this.age = age;
    this.hasWorkPermit = hasWorkPermit;
    this.languages = languages;
}
// Initialise object
var bellBoy1 = new BellyBoy("Timmy", 19, true, ["French", "English"]);
```
```
Exercise: Create a new object hosekeeper1 and tap in to it and his properties by using the dot notation.
Challenge: Create a constructor function for the houseKeeper1, so instead of creating it one by one use
the constructor for any houseKeeper object, and then to create the object houseKeeper1 using that constructor
function.
```
```javascript
//Create object
var houseKeeper1 = {
    yearsOfExperience: 12,
    name: "Jane",
    cleaningRepertoire: ["bathroom", "lobby", "bedroom"]
}
//Acces to its properties
console.log(houseKeeper1.name)
```
```javascript
//Constructor function
function HouseKeeper (name, yearsOfExperience, cleaningRepertoire) {
    this.name = name;
    this.yearsOfExperience = yearsOfExperience;
    this. cleaningRepertoire = cleaningRepertoire;
}
//Initialise object
var houseKeeper1 = new HouseKeeper("Bartolomeu", 120, ["Porgraming", "Medicine", "Astronaut"]);
```

## How to use switch statements
```
Railroad switch: Switch statements it will take the code down a different track depending on the value of a variable
Whate we going to switch on
```
```javascript
switch (expresion) { //Switch the letter that is inside the innerHTML
    case expresion:
    //code;
    break:
    default:
 }
```
```javascript
var buttonInnerHTML = this.innerHTML;
switch(buttonInnerHTML){
    case "w":
    //play audio w
    break; //Every case start with ":" and end with "break;"
    //Break tells the code to exit the swithc statement and continue with the rest of the code
```
```
We recommend to give your sound audio diferent name, asociated with the seound they make
Remember change it in all the parts that are afected like audio.play to tom1.play()
```
```
The "default" part is kind of like the "else" statement at the end of an "if"
Its a good practice to specify something
```
```javascript
default:console.log(buttonInnerHTML)
```

## Objects, their methods and the dot notation
```
Methods
If we wanted our object to also have an associated function then all we have to do is provide the
name of the function as a new parameter and then colon, and then after the colon we just put in the
anonymous function.
```
```javascript
var bellBoy1 = {
    name:"Timmy",
    age: 19,
    hasWorkPermit: true,
    languages:["French", "English"],
    moveSuitcase: function () { // Method
        alert("May I take your suitcase");
        pickUpSuitcase(); //This is for demostration porpouses
        move(); // Also for demostration porpouses
    }
```
```
And now our bellBoy1 has a method, wich remember is just a function that's associated with an object
```
```
Call Method
When using properties or calling a method we're always using the dot notation.
```
```javascript
bellBoy1.moveSuitcase(); //The only difference that you see between method and the property are those parentheses
```
```
Constructor function incorporate the method in to our construction function
```
```javascript
function BellBoy(name,age...) {
    this.name = name;
    this.age = age;
    ...
    this.moveSuitcase = function() {
        //code;
    }
}
```
```
Challenge: add a method to our HoseKeeper constructor function and this method is just called clean
simplified so that our method send an alert says "cleaning in progress", construct the object and then
call the cleaning method associated with that new object.
```
```javascript
//This is the constructor function
function HouseKeeper (name, yearsOfExperience, cleaningRepertoire) {
    this.name = name;
    this.yearsOfExperience = yearsOfExperience;
    this.cleaningRepertoire = cleaningRepertoire;
    this.clean = function() {
        alert("cleaning in progress");
    }
}

//This is how we create a new object using the constructor function
var houseKeeper1 = new HouseKeeper ("Monika", 20, ["Bathroom", "Kitcher", "Bed Room"]);

//This is how we call the cleaning method associated with the new object, and we can call any property or method using the dot
houseKeeper1.clean();
```
```
Reviewing the "How to play sounds on a website" chapter, about the "play()" method and how it works
```
```javascript
//Create new Audio object and pass the sound file location
var tom1 = new Audio("sound/tom-1.mp3");

//We used that object method called "play()" to play that sound
tom1 = play();

//Constructor function whith which play() is associated
function Audio (fileLocation){
    this.fileLocation = fileLocation;
    this.play = function() {
        //Tap in to the audio hardware
        //Check the file at fileLocation exist
        //Check the file at fileLocation is a sound file
        //Play the file at fileLocation
    }
}
```

## Using keyboard Event Listener to check for Keypress/Keydown
```
For the buttons we can add an EventListener to the html elements that represent the buttons
but what exactly do we add this "keydown" event listener to?
You can add an event listener to the entire document, so that the entire web page starts listening
for keyboard strokes.
```
```javascript
document.addEventListener("keydown", function (){
    alert("key was pressed")
});
```
```
How do we figure out wich key was pressed?
```
```javascript
addEventListener("keydown", function (event){ //The "event" is the parameter
    console.log(event); //You can alswo try event.key to acces the key property inside the event
});
```
```
In order tu fully understand this part of the code we have to understand how in Javascript
we can pass function as parameters and we can also have function as callbacks, include things
that we get back afther the event has happend
```
```
Challenge: Create a function that takes a character and checks it agains the switch in order to play the correct sound.
And then we're going to call it inside the event listener for the key pressed as well as the event listener for our drum buttons
```
```javascript
//Detecting Button Press
for (let count = 0; count < document.querySelectorAll(".drum").length; count++) {
    document.querySelectorAll(".drum")[count].addEventListener("click", function(){
        var buttonInnerHTML = this.innerHTML; 
        makeSound(buttonInnerHTML);    
    })
}
//Detecting Keyboard Press
document.addEventListener("keydown", function (event) {
    var keypress = event.key;
    makeSound(keypress)
});
//Make sound
function makeSound(key){
    switch (key) {
        case "w":
            var tom1 = new Audio("./sounds/tom-1.mp3");
            tom1.play();
            break;
        case "a":
            var tom2 = new Audio("./sounds/tom-2.mp3");
            tom2.play();
            break;
        case "s":
            var tom3 = new Audio("./sounds/tom-3.mp3");
            tom3.play();
            break;
        case "d":
            var tom4 = new Audio("./sounds/tom-4.mp3");
            tom4.play();
            break;
        case "j":
            var snare = new Audio("./sounds/snare.mp3");
            snare.play();
            break;
        case "k":
            var crash = new Audio("./sounds/crash.mp3");
            crash.play();
            break;
        case "l":
            var kickBass = new Audio("./sounds/kick-bass.mp3");
            kickBass.play();
            break;
    
        default: console.log(buttonInnerHTML)
            break;
    } 
}
```
