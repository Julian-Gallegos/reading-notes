# **Read: Class 03**
### Reading Notes Assignment on Lists, Keys, the Spread Operator, and How to Pass Functions Between Components
  [Link back to main reading notes page](https://julian-gallegos.github.io/reading-notes/)

## .map() and the spread operator are powerful and important tools for React, but also for JavaScript as a whole due to their efficient and highly readable functionality when creating or unpacking groups of elements.

## React Docs - Lists and Keys:

source credit: https://reactjs.org/docs/lists-and-keys.html and https://reactjs.org/docs/reconciliation.html#recursing-on-children
   1. What does .map() return?
      - `Array.map()` returns a new array populated with the results of calling a provided/callback function on each element in its calling array.
   2. If I want to loop through an array and display each value in JSX, how do I do that in React?
      - {array.map(element => do thing returns a value);} // curly brace wrapper allows this to be called in the middle of jsx
   3. Each list item needs a unique ____.
      - key
   4. What is the purpose of a key?
      - Keys give elements a stable identity, which is important for optimizing React when recursing on the children of a DOM node.
## The Spread Operator:

source credit: https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab
   1. What is the spread operator?
      - Syntax that allows iterables like arrays or strings to be expanded in places where zero or more arguments/elements for function calls/array literals are expected. If used in an object literal, spread enumerates the properties of the object and adds key-value pairs to the object being created.
   2. List 4 things that the spread operator can do
      - Copy arrays, concatenating arrays, populating arguments for a function from an array/using an array as arguments, and converting NodeLists into arrays.
   3. Give an example of using the spread operator to combine two arrays.
      
      `
      const array1 = [1,2,3];
      const array2 = [4,5,6];
      const concatenated = [...array1,...array2];
      console.log(...concatenated); // 1 2 3 4 5 6
      `
   4. Give an example of using the spread operator to add a new item to an array.
      
      `
      const array1 = [4,5,6];
      const array2 = [1,2,3,...array2];
      console.log(array2); // [1, 2, 3, 4, 5, 6]
      `
   5. Give an example of using the spread operator to combine two objects into one.
      
      `
      const object1 = {fizz: "hello"}
      const object2 = {buzz: "world"}
      const combined = {...object1,...object2}
      console.log(combined); // Object { fizz: "hello", buzz: "world" }
      `
## How to Pass Functions Between Components:

source credit: https://www.youtube.com/watch?v=c05OL7XbwXU
   1. In the video, what is the first step that the developer does to pass functions between components?
      - pass the function into the component like any other prop.
   3. In your own words, what does the increment function do?
      - Assuming this question refers to the increment in Person.js, it sets the state of hasChanged to true, which, through an if/&& check in the jsx, causes a span element to be included in the rendered html from jsx. After that, increment calls this.props.increment, the passed in function that is at the top level of the components, which will then cause a state change and increment the count associated with whatever button was clicked.
   4. How can you pass a method from a parent component into a child component?
      - The same way any props are passed, declare and define it from the parent, then pass it as a prop within the jsx call to the child component.
   5. How does the child component invoke a method that was passed to it from a parent component?
      - this.props.functionName().
## Things I want to know more about
   1. What does the algorithm for the spread operator look like "under the hood"? I have my guesses but it would be cool to know.
   2. The code in the video on passing functions between components calls setState() twice each time the displayed add buttons are pressed. Is this inefficient compared to an implementation that calls setState() once on all state variables at the same time? Would this cause multiple rerenders, or doees React batch the state changes before rerendering? 
