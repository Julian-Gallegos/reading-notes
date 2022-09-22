# **Read: Class 04**
### Reading Notes Assignment on Controlled Components and The Ternary Operator
  [Link back to main reading notes page](https://julian-gallegos.github.io/reading-notes/)

## Knowing more about controlled components is important for following React design practices while stilll making use of our prior knowledge on html input elements. Knowing and using the ternary operator is good for writing eloquent code. The ternary operator is very commonly used, so knowing how to read it is important to improve one's ability to read the code of others.

## React Docs - Forms

source credit: https://reactjs.org/docs/forms.html
   1. What is a ‘Controlled Component’?
      - A controlled component is an html input element that accepts user input and has functions that use React setState() handle the state change for the input. 
   3. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
      - In terms of performance, the application will need to rerender each time state is updated, so it is better to wait to store the users responses then update on submit. However doing this would not follow the "single source of truth" logic of controlled components, and the form would still rerender anyway, which React might be able to batch its state change with the form rerender, but I'm not sure about that.
   5. How do we target what the user is entering if we have an event handler on an input field?
      - give the handler an argument called something like `event` and it will pass in all the data needed. within the handler function the value on change is fetched with `event.target.value`

## The Conditional (Ternary) Operator Explained

source credit: https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff
   1. Why would we use a ternary operator?
      - The ternary operator syntax is much cleaner and shorter than if condition syntax, especially when performing many short else if conditionals.
   2. Rewrite the following statement using a ternary statement:

`
if(x===y){
  console.log(true);
} else {
  console.log(false);
}
`
      - Ternary version:     
`
x===y ? console.log(true) : console.log(false);
`
      - This is maybe a bit cleaner, but this would actually be even better without the ternary operator:
`
console.log(x===y);
`
      
## Things I want to know more about
   1. If I update a form html element with a React based function handler, does the Form independently rerender from the state rerender? In other words, will there be two rerenders, one for the independent state of the form, and another for the react setState rerender?
