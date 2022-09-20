# **Read: Class 02**
### Reading Notes Assignment on React's Lifecycle and States Vs Props
  [Link back to main reading notes page](https://julian-gallegos.github.io/reading-notes/)

## Knowing the lifecycle of React components is important for mastering React, as a better understanding allows us to optimize our code and dataflow via the methods React provides us. Comparing the differences between state and props makes us more aware of the role they play in the design and implementation of well designed React apps. A particularly noteworthy fact is that an application is re-rendered after updating a component's state. If one were uninformed on this fact, one could easily design inefficient or slow code that causes many unnecessary re-renders.

## Component-Based Architecture Questions:
   1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
      - ‘render’ happens before ‘componentDidMount’.
   2. What is the very first thing to happen in the lifecycle of React?
      - The constructor is called, then static getDerivedStateFromProps is called.
   3. Put the following things in the order that they happen: 
      1. `constructor`
      2. `render`
      3. `componentDidMount`
      4. `React Updates`
      7. `componentWillUnmount`
   4. What does `componentDidMount` do?
      - This method is called immediately after a component is mounted, meaning it can be used to initialize the DOM or load things using network requests.
## What is Props and How to Use it in React:
   1. What types of things can you pass in the props?
      - One can pass data through props similar to how one can pass arguments to a function. For example, numbers or strings.
   2. What is the big difference between props and state?
      - State is handled inside of a component and can be updated within the component while props are handled outside of a component and can only be updated outside of the component before being passed into it.
   3. When do we re-render our application?
      - A section of the application must be re-rendered when a state is changed within it.
   4. What are some examples of things that we could store in state?
      - Anything that can be updated by the user:
        - Forms
        - A counter application, as it tracks and updates its count
        - Radio lists
        - Check lists
        - Functionality that might be attached to buttons or other DOM elements
      
## Things I want to know more about
   1. I think I understand the function of `componentDidMount`, but I think I would have a better understanding of its purpose if I saw some more examples of it in use.
