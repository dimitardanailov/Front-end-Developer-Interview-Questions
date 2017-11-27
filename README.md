# Front-end Developer Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

Note: Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

1) 

> Q: Explain event delegation
> A: JS event listeners fire not only on a Single DOM element but on all its descendants

2) 

> Q: Describe event bubbling
> A: Inverse of this. Also known as propogation, events on an element will "bubble up" and also fire on all parents

Bonus)

> Q: What's the difference between `target` and `currentTarget` ?
> A: The latter is the element with the listener attached, the former is the actual element that triggered it.

```javascript
function handleChange(event) {
  // track your change
  console.log(event.currentTarget.value);
}

const formEls = document.getElementByTagName('input');

for (var i = 0; i < formEls.length; i++) {
  formEls[i].addEventListener('change', handleChange, false);
}
```

```javascript
function handleChange(event) {
  // track your change
  // this time on e.target
  console.log(event.target);
}

const element = document.getElementById('form');
element.addEventListener('change', handleChange);
```

3) 

> Q: Explain why the following doesn't work as an IIFE:

```javascript
function foo() {
  // i puty this code
}();
```

> IIFE - Immediately invoked function expression

 4) 
 
 > Q: Explain the difference on the usage of: 

```javascript
function foo() {
  // i am known as 
  // a definition or statement
}

var foo = function() {
  // i am an expression
  // i resolve to a value, even if just "undefined"
}
```

> MDN - An expression is any valid unit of code that resolves to a value.

```javascript
/* Functions as expressions vs definitions */

// this thing here
function foo() {

}();

// is as if you
function foo() {
}

();
// wrote it on separate line
```
