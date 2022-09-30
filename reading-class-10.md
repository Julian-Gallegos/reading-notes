# Read Class 10: JavaScript Call Stack and Error Messages
  [Link back to main reading notes page](https://julian-gallegos.github.io/reading-notes/)


## Why this topic matters

Understanding the Call Stack is vital to understanding programming, as it plays a key role in the data flow for functions, and will be important for understanding more advanced programming concepts like recursion, and even the memory stack.
Understanding error messages is important for debugging code, something every programmer will be doing a lot of.


## JavaScript Call Stack

source credit: [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)
   
   
   1. **What is a ‘call’?**

A call is when a function is used/invocated during a program. The scope of the program changes to that of the code within the function, with the names of any declared variables within the function going out of scope once the program leaves a function.

   
   2. **How many ‘calls’ can happen at once?**

The call stack is a single stack data structure in memory, therefore only one call can be made at a time.
  

   3. **What does LIFO mean?**

Last In First Out. It is the algorithm structure of a stack. In detail, when an item gets pushed into the stack (in the case of this reading, a call to a function), it will remain in the stack until it is popped out of the stack. If multiple items are pushed into the stack and we try to pop something out of the stack, only the most recent item added to the stack can be removed, followed by the next most recent, and so on. This functionality works very similarly to a real life stack of objects, where one will have the easiest time grabbing from the top of the stack.


   4. **Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.**
     
I don't think I can post a drawing on the replies in canvas, but if we put it sideways for text format it would be like this with `function3()` as the first function called:  

`Pop from here <- function1() <- function2(){call function1} <- function3(){call function2}`


   5. **What causes a Stack Overflow?**

Usually a recursive function with no exit point, but the Call Stack does have a memory limit, so technically it's possible to cause a stack overflow with a VERY long series of function calls, which again would most likely happen with recursive functions.


## JavaScript Error Messages

source credit: [JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)
   
  
   1. **What is a ‘reference error’?**

An error that occurs when trying to use a variable that has not been declared.



   2. **What is a ‘syntax error’?**

An error that occurs when the compiler parses through code that breaks the code grammar rules for its language or data type, such as an improperly written JSON 



   3. **What is a ‘range error’?**
 
An error that occurs when trying to manipulate an object outside of its valid length, for example, trying to access the 5th index of an array with a length of 3. Can also occur when trying to set an invalid length for an object.
  
  
   4. **What is a ‘type error’?**
  
An error that occurs when treating some data or variable as a type that it is not. For example, trying to call Array functions with a non array type variable, like this:

    let str = `I'm a string`;
    let this_will_cause_an_error = str.map(garbage => none of this will work);
  
  
   5. **What is a breakpoint?**
  
A designated point in a file's code that tells a debugger to pause the running code at that point and display debug info relating to that point.
  
  
   6. **What does the word ‘debugger’ do in your code?**

`debugger` is a statement that will set a breakpoint in your code.


## Things I want to know more about
   1. I learned a lot about this in school, so I can't honestly come up with something relevant and new to ask about... I guess I'm curious if there is any popular debugger software for node.js like GNU Debugger.
