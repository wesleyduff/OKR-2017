# OKR
## Promises
## Async Functions
## Strict Mode

### Promises

A Promise is an object that is used as a placeholder for the eventual results of a deferred (and possibly asynchronous) computation.
An alternative to callbacks for delivering the results of an asynchronous computation.
Promise has been spec that has been created called [Promise/A+](https://promisesaplus.com/)
There are frameworks for you to use which include
+ [Q](https://github.com/kriskowal/q)
+ [Bluebird](https://github.com/petkaantonov/bluebird)
+ [RSVP](https://github.com/tildeio/rsvp.js)

With ES6 and Babel, there is no need to use a framework.

A promise can be in three states
+ pending
+ fulfilled
+ rejected
A promise is pending if it is neither fulfilled nor rejected.

```javascript

//anync func
function asyncFunction(){
  return new Promise(
    function(resolve, reject){
      if(x){
        resolve(result);
      } else {
        reject(result)
      }
    }
  )
}

//call async func as show
asyncFunction()
.then(result => {...})
.catch(error => {...});
```

#### .then()
Always returns a Promise, alows you to chain method calls.



links:
+ [es6 defs on promises](https://tc39.github.io/ecma262/#sec-promise-objects)
+ [Wikipedia on Promises](https://tc39.github.io/ecma262/#sec-promise-objects)

*FAQs*
+ promises start off in the pending state
++ promise is then fulfilled or rejected. This state is referred to as **settled** and is not pending any longer.
++ promise is then sent to one of two methods, fulfillReactions(result), rejectReactions(error) instead of success and failure actions.
