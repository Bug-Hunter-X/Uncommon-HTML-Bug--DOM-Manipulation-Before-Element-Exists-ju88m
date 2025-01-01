# Uncommon HTML Bug: DOM Manipulation Before Element Exists

This repository demonstrates a common error in HTML/JavaScript web development where JavaScript code tries to manipulate a DOM element before that element has been fully parsed and added to the DOM tree. 

## Bug Description

The bug is present in `bug.html`. JavaScript code attempts to modify the `innerHTML` of a div element with the ID 'myDiv' before the browser has finished rendering the div. This results in an error because `document.getElementById('myDiv')` returns null, leading to an error.

## Solution

The solution is provided in `bugSolution.html`. The JavaScript code is wrapped inside a `DOMContentLoaded` event listener. This ensures the script executes only after the entire HTML document is parsed and the DOM is ready.