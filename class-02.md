### Atomic Design pt1
This article had to do with looking at a page and separating out different elements. The first level of separation was the 'organisms' which are the biggest parts of the page an example would be like a header section or a side bar section. After that the next phase is breaking those down into 'molecules' which might be the nav component that has our nav links in the header. Then we go to the 'atomic' level which is each individual link in the nav bar. That is the last step as breaking links into smaller pieces doesn't make sense. 

### Atomic Design pt2
The main point of the article was when starting to build your app using atomic design the code is done from the smallest component up to the largest which is the opposite of breaking down a site atomically. Then it ran through actually doing that for the example site. 

### Thinking in react step 1
When designing its best to identify the main components of the app and have a sense of what the parent and child components are.


### UI components by design
'Components let you split th UI into independent, reusable pieces and think about each piece in isolation. Break down a UI in hierarchies and design them for consistency.
Design patterns have create an emergence of common language between designers and developers. 

 Two types of components 
 1. Foundation components 
 - the primary expressiong of the design language of the system?
 1. Application components are specific to one of the applications being built and not seen as a dfefining foundational part of the UI.. 
 
 When building its a good idea to start with the foundation components and as that gets solidified, the application components can then be focused on to better determine where in the page they will work best.
 
 
 ### What are Javascript callbacks 
 Functions can take functions as arguments and can be returned by other functions. Functions that do this are called higher order functions.
 - callback functions
 
 Callbacks are a way to make sure certain code doesnt execute until other code has finished execution.
 
 ```
 function doHomework(subject, callback) {
  alert(`Starting my ${subject} homework.`);
  callback();
}

function alertFinished(){
  alert('Finished my homework');
}

doHomework('math', alertFinished);
```

### First Class Functions

 First class function is one that is treated like any other ordinary variable, in such a language functions can be passed as an argument to other functions, and can be returned by another function and can be assigned as a value to a variable. 
 ```
 function sayHello() {
   return "Hello, ";
}
function greeting(helloMessage, name) {
  console.log(helloMessage() + name);
}
// Pass `sayHello` as an argument to `greeting` function
greeting(sayHello, "JavaScript!");
```

In this example; We need to return a function from another function - We can return a function because we treated function in JavaScript as a value.
```
function sayHello() {
   return function() {
      console.log("Hello!");
   }
}
```
We can also set variables equal to a function and call the variable as if it were a function
```
const sayHello = function() {
   return function() {
      console.log("Hello!");
   }
}
const myFunc = sayHello();
myFunc();
```

We are using double parentheses ()() to invoke the returned function as well.
```
function sayHello() {
   return function() {
      console.log("Hello!");
   }
}
sayHello()();
```


### MDN callback function

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or actions 

```
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
```

 
