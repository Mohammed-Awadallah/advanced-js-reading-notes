##  What are React Hooks?

_With the new addition of hooks( along with React 16.8), functional components could maintain states and lifecycle features without using classes. Simply hooks are features that allow you to “hook into” React state and lifecycle features from function components._

**The below code segment shows the basic signature for a normal functional component, and we can hook into a particular state using this hook concept.**

     function Example(props) {  
	// Hooks can be used here  
	return <div />;  
	} 

## Why We Need React Hooks?
Previously, If you write a function component and notice that you need to apply some state to it all you have to do is, change that functional component into a class.
> _But with the new update, you can just use a Hook inside the function component, making the refactoring procedure easy._

also, there are many advantages of using React hooks like:

-   More flexibility in reusing an existing piece of code.
-   There is no need to refactor the functional component into a class component when it grows complex.
-   You don’t have to worry about this at all.
-   No more bindings for methods
-   It is simpler to distinguish logic and UI using hooks.

## React Hook Types
It is possible to divide the built-in hooks into two sections, which are given below. React offers a few built-in hooks, such as

## **Basic Hooks**

-   `useState()`
-   `useEffect()`
-   `useContext()`

## **Additional Hooks**

-   `useReducer()`
-   `useMemo()`
-   `useCallback()`
-   `useImperativeHandle()`
-   `useDebugValue()`
-   `useRef()`
-   `useLayoutEffect()`

### State Hook

Let’s get started by  `useState`  Hook from React.
In a class, by setting  `this.state`  to { age: 0 } in the constructor, we initialize the age state to 0.

	class Sample extends React.Component {  
	  constructor(props) {  
    super(props); this.state = {  
	     age: 0  
	   };  
	 }
	
Since we are not using  `this.state`  inside the functional component, we have to call the  `useState`  hook directly through our functional component.

	import React, { useState } from 'react';function Sample() {  
	  // Initialize a new state variable called  "age"  
	  const [age, setAge] = useState(0);
