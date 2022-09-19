# **Read: Class 01**
### Reading Notes Assignment on React's Component Architecture and Props
  [Link back to main reading notes page](https://julian-gallegos.github.io/reading-notes/)

## This topic is important as props and components are the basic structure for every React app. React is extra important to know in general due to its widespread use in the dev community.

## Component-Based Architecture Questions:
   1. What is a “component”?
      > A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.
        
      Quoted from the [tutorialspoint article on components](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm) under the section on "What is a component?"
      - In my own words, I take this to mean that they are well organized groups of functional code intended to be used as interface code for generalized use. They seem similar to regular functions, but they specifically return html.
   2. What are the characteristics of a component?
      - Reusability: Components are designed to be reusable across different applications and situations within each application.
      - Replaceable: Ideally no issues should arise when replacing one component with other similar components.
      - Not context specific: 
      > Components are designed to operate in different environments and contexts.
      
      Quoted again from the [tutorialspoint article on components](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm) under the section on "Characteristics of Components"
      - Extensible − A component can extend from other components in the same way that classes can extend from other classes, allowing newly defined behaviors from existing existing components.
      - Encapsulated − Components can be called to provide their functionality without exposing details such as their internal variables, processes, or state.
      - Independent − Components have minimal dependencies on other components.
   3. What are the advantages of using component-based architecture?
      - Many of the characteristics of components are advantagous. Components are well encapsulated and therefore make systems that rely on them more reliable and reusable as a whole, which in turn reduces costs. They also allow for easier deployment as replacing existing versions will have no impact on other components through their independency.  

## What is Props and How to Use it in React:
   1. What is “props” short for?
      - Properties
   2. How are props used in React?
      - Props are passed into React components to pass along data, following React's one-way dataflow
   3. What is the flow of props?
      - One-way, from parent to child.
      
## Things I want to know more about
   1. I think I have a surface level understanding of components, but I think they'll make more sense when I've shown a specific example of a component. EDIT: After looking over some of the lab materials, the added visualization has helped a lot for understanding components.
