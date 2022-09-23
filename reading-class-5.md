# Read Class 05: Thinking in React and Higher Order Functions.
  [Link back to main reading notes page](https://julian-gallegos.github.io/reading-notes/)


## Why this topic matters

The article on thinking in React is very important as it exposes us to important design principles and how they apply to React. Following good design principles leads to easier to code that is easier to understand, faster to implement, and less prone to bugs.
Riding off the goal of cleaner, less error prone code brings us to why higher-order functions are important. The eloquent JavaScript article on higher-order functions is all about abstraction, the act of hiding away complicated details to instead talk about problems at a higher (more abstract. Higher-level functions allow us to abstract over actions.
Through abstraction, a program can be shortened into cleaner, more readable groups of code, leaving less room for error when programmers try to understand and build upon the code.


## React Docs - Thinking in React

source credit: https://reactjs.org/docs/thinking-in-react.html and https://en.wikipedia.org/wiki/Single-responsibility_principle
   
   
   1. What is the single responsibility principle and how does it apply to components?

The single responsibility principle states "A module should be responsible to one, and only one, actor." 

--Martin, Robert C. (2018). Clean architecture : a craftsman's guide to software structure and design. Boston. ISBN 978-0-13-449432-6. OCLC 1003645626

The module being a component in the case of React. The component should only perform one thing, and if it grows beyond that, it should be split into smaller subcomponents.

   
   2. What does it mean to build a ‘static’ version of your application?

A static version of an application renders its UI and any data model it already has with it, but does not include any interactivity/state change functionality.


   3. Once you have a static application, what do you need to add?

This is the part where one adds the minimal representation of the UI's state. This meaning one has to consider the minimum set of mutable states that the app needs, then implement them.


   4. What are the three questions you can ask to determine if something is state?
     
      1. Is it passed in from a parent via props? If so, it probably isn’t state.
      2. Does it remain unchanged over time? If so, it probably isn’t state.
      3. Can you compute it based on any other state or props in your component? If so, it isn’t state. 


   5. How can you identify where state needs to live?

      1. Identify every component that renders something based on that state.
      2. Find a common owner component (a single component above all the components that need the state in the hierarchy).
      3. Either the common owner or another component higher up in the hierarchy should own the state.
      4. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.


## Higher-Order Functions

source credit: https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK
   1. What is a “higher-order function”?

A higher-order function is a function that either takes other functions as arguments or returns them.


   2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

Line 2 is returning an anonymous arrow function that takes an argument `m` and returns the resolved boolean value for the expression `m > n` where n is a number passed in as an argument from the higher-order function `greaterThan()`.


   3. Explain how either map or reduce operates, with regards to higher-order functions.

`.map()` operates as a higher-order function as a callback function must be passed into it as an argument for it to function. This callback function will be called on each array element from the array that calls `.map()`.


## Things I want to know more about
   1. `reduce()` seems useful. I'd like to go through the `characterCount()` function mentioned in the eloquentjavascript article on higher-order functions as it was confusing.
