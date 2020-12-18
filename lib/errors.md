# JavaScript Errors and Debugging

Each code snippet below throws an error. Your task is to determine (a) what is
the error message, (b) what is causing the error message and (c) how to resolve or fix the error?

## Errors

### Prompt #1

We want an alert to appear in the browser that says "Hello World". But for some
reason, it's not working ...

```js
alert(greeting);
```

A. What is the error message?
ReferenceError: greeting is not defined
B. What is causing the error?
No quotes around the word "greeting"
C. How can you resolve/fix the error?
Put quotes around greeting
```js
alert('"Hello World"');
```

### Prompt #2

We're trying to log the birds with names that are more than 4 characters long.
But for some reason, it's not working ...

```js
let birds = ['Eagle', 'Falcon', 'Duck', 'Turkey']

birds.forEach(function(bird) {
  if (bird.length > 4) {
    console.log(bird)
}
```

A. What is the error message?
No error message.  No output. Then Uncaught SyntaxError: missing { before function body.
B. What is causing the error?
Missing closing brackets at end of code.
C. How can you resolve/fix the error?
put in brackets.
```js
let birds = ['Eagle', 'Falcon', 'Duck', 'Turkey']

birds.forEach(function(bird) {
  if (bird.length > 4) {
    console.log(bird)
  }
})
```

### Prompt #3

We're trying to concatenate these two strings together. But for some reasons,
it's not working ...

```js
let greeting = "hello";
greeting.push(" world");
console.log(greeting);
```

A. What is the error message?
Uncaught TypeError: greeting.push is not a function
B. What is causing the error?
Push is an array function.  No array.
C. How can you resolve/fix the error?
Missing brackets to allow push to work.  Add brackets around hello.  Also had to add join to get stings to concatenate.
```js
let greeting = ["hello"];
greeting.push (" world");
console.log(greeting.join(""));
```

### Prompt #4

We're trying to call the `greet` function. But for some reason, it's not working
...

```js
this.greet();
```

**Hint:** What is `this` in the global scope in our browser?
// Needs to be a property of an object.  Move on for now.
A. What is the error message?
Uncaught TypeError: this.greet is not a function
B. What is causing the error?

C. How can you resolve/fix the error?

```js
this.greet();
```

### Prompt #5

We're trying to print Bob's name to the console. But for some reason, it's not
working ...

```js
var bob;
console.log(bob.name);
```

A. What is the error message?
Uncaught TypeError: bob is undefined
B. What is causing the error?
object.name was not defined
C. How can you resolve/fix the error?
define variable bob with name in brackets.
```js
var bob = {
   name: "Bob" 
};
console.log(bob.name);
```

### Prompt #6

We're trying to print the message to the console. But for some reason, it's not
working...

```js
  let forSale = "sea shells"
  let message = `She "sells' ${forSale} by \`sea' sea shore'
  console.log(message)
```

A. What is the error message?
Uncaught SyntaxError: `` literal not terminated before end of script
B. What is causing the error?
Improper puncuation in message.  Need back tics.
C. How can you resolve/fix the error?
Back ticks and elimate other punctuation.  replace sea with the.
```js
  let forSale = "sea shells"
  let message = `She sells ${forSale} by the sea shore`
  console.log(message)
```

### Prompt #7

We're trying to print Bob's first name to the console. But for some reason, it's
not working.

```js
const bob = {
  profile: {
    name: {
      firstName: "Bob",
      lastName: "Seger"
    },
    age: 73,
    dateOfBirth: {
      month: "May",
      day: 6,
      year: 1945
    },
    career: "Singer"
  }
};

console.log(bob.name.first_name);
```

A. What is the error message?

B. What is causing the error?

C. How can you resolve/fix the error?

```js
const bob = {
  profile: {
    name: {
      firstName: "Bob",
      lastName: "Seger"
    },
    age: 73,
    dateOfBirth: {
      month: "May",
      day: 6,
      year: 1945
    },
    career: "Singer"
  }
};

console.log(bob.name.first_name);
```

### Prompt #8

We're trying to make it so that when we call the `greet` method of `person`, an
alert appears with the person's full name. But for some reason, it's not working
...

```js
let person = {
  firstName: "Bob",
  lastName: "Seger",
  greet: function() {
    function fullName() {
      return `${this.firstName} ${this.lastName}`;
    }

    alert(fullName());
  }
};

person.greet();
```

A. What is the error message?

B. What is causing the error?

C. How can you resolve/fix the error?

```js
let person = {
  firstName: "Bob",
  lastName: "Seger",
  greet: function() {
    function fullName() {
      return `${this.firstName} ${this.lastName}`;
    }

    alert(fullName());
  }
};

person.greet();
```

### Prompt #9

We're trying to implement the [Fibonacci Sequence](https://en.wikipedia.org/wiki/Fibonacci_number). But for some reason,
it's not working ...

**Note:** The commented out code is part of the prompt. It represents code we've tried to implement to complete the function, and we may or may not need all or some of the commented out code in the final solution.

```js
function createSequence( max ) {
  let sequence = [1, 1]
  // a = 1
  // b = 1

  for (let i = 2; i < max; i++) {
  let a = sequence[i - 1]
  let b = sequence[i - 2]
  sequence.push(a + b)

  // while (i <= max) {
  //    var a = 1, b = 1
  // }
  // }
  return sequence
}

let sequence = createSequence(20)
console.log(sequence)
```

A. What is the error message?

B. What is causing the error?

C. How can you resolve/fix the error?

```js
function createSequence( max ) {
  let sequence = [1, 1]
  // a = 1
  // b = 1

  for (let i = 2; i < max; i++) {
  let a = sequence[i - 1]
  let b = sequence[i - 2]
  sequence.push(a + b)

  // while (i <= max) {
  //    var a = 1, b = 1
  // }
  // }
  return sequence
}

let sequence = createSequence(20)
console.log(sequence)
```

### Prompt #10

We're trying to make a working counter object. But for some reason, it's not
working ...

```js
const Counter = {
  total: 0,
}

Counter.increase() {
  this.total++
}

Counter.decrease() {
  this.total--
}

Counter.reset() {
  this.total = 0
}

Counter.increase()
Counter.increase()
Counter.increase()
Counter.increase()
Counter.increase()
Counter.increase()
console.log(Counter.total) // => value = 6
Counter.decrease()
Counter.decrease()
Counter.decrease()
Counter.decrease()
console.log(Counter.total)  // => value = 2
Counter.rest()
console.log(Counter.total) // => value = 0
```

A. What is the error message?

B. What is causing the error?

C. How can you resolve/fix the error?

```js
const Counter = {
  total: 0,
}

Counter.increase() {
  this.total++
}

Counter.decrease() {
  this.total--
}

Counter.reset() {
  this.total = 0
}

Counter.increase()
Counter.increase()
Counter.increase()
Counter.increase()
Counter.increase()
Counter.increase()
console.log(Counter.total) // => value = 6
Counter.decrease()
Counter.decrease()
Counter.decrease()
Counter.decrease()
console.log(Counter.total)  // => value = 2
Counter.rest()
console.log(Counter.total) // => value = 0
```

### Prompt #11

We're trying to print the string `"hello world"`. But for some reason, it's not
working ...

```js
let obj = {
  oompa: [
    {
      loompa: {
        doopati: [
          [
            {
              do: ["good by cruel world", "hello world", "goodnight moon"]
            }
          ]
        ]
      }
    }
  ]
};

let message = obj[0].oompa.loompa[0].doopati.do[2];
console.log(message);
```

A. What is the error message?

B. What is causing the error?

C. How can you resolve/fix the error?

```js
let obj = {
  oompa: [
    {
      loompa: {
        doopati: [
          [
            {
              do: ["good by cruel world", "hello world", "goodnight moon"]
            }
          ]
        ]
      }
    }
  ]
};

let message = obj[0].oompa.loompa[0].doopati.do[2];
console.log(message);
```
