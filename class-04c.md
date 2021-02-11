# Javascript Asyncronous Programming and Callbacks

###Callbacks
The function that is called when an event is triggered and has an attached event listener to the event
Javascript `first class functions` can be passed as variable to other functions (higher-order functions)

It’s common to wrap all your client code in a load event listener on the window object, which runs the callback function only when the page is ready

Using the `setTimeout()` is another useful example of a callback function


### Handlingg errors in callbacks
Node js adopted a syntax  where: the first paramete in any callback function is the error object `error-first callbacks` as they're known
If there is no error the object is null
```
fs.readFile('/file.json', (err, data) => {
  if (err !== null) {
    //handle error
    console.log(err)
    return
  }

  //no errors, process data
  console.log(data)
})
```

#### A problem with callbacks
they quickly become confusing to read as your code has more nested callbacks

Some alternatives are *promises* *async/await*


# Understanding Javascript Promises

A promise is commonly defined as a proxy for a value that will eventually become available

`Async functions` use the promises API as their building block, so understanding them is fundamental even if in newer code you’ll likely use async functions instead of promises.
This is what a promise looks like 
```
let done = true

const isItDoneYet = new Promise((resolve, reject) => {
  if (done) {
    const workDone = 'Here is the thing I built'
    resolve(workDone)
  } else {
    const why = 'Still working on something else'
    reject(why)
  }
})
```
the promise evaluates the done global variable if true, returns a resolved promise, otherwise returns a rejected promise
`resolve` and `reject` is how we communicate back a value.


### How to USE a promise
```
const isItDoneYet = new Promise()
//...

const checkIfItsDone = () => {
  isItDoneYet
    .then(ok => {
      console.log(ok)
    })
    .catch(err => {
      console.error(err)
    })
}
```
Running checkIfItsDone() will execute the isItDoneYet() promise and will wait for it to resolve, using the then callback, and if there is an error, it will handle it in the catch callback.

### Chaining promises
The Fetch API is a layer on top of XMLHttpRequest API, it can be used to chain together multiple promises into chains 

### Handling Errors
When anything in the chain of promises fails it'll raise an error or reject the promise, so the control goes down chain to the nearrest `catch()`
Just like promises multiple catches can be chained together to handle errors inside the parent `.catch`

We can synchronize different promises together to define a list of promise to execute code when they resolve. 

`Promise.race()` runs as soon as one of the promises you pass to it resolves, and it runs the attached callback just once with the result of the first promise resolved.


### Uncaught TypeError: undefined is not a promise
You're probably using `Promise()` and not `new Promise()`



















