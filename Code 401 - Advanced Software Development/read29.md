# Review, Research, and Discussion
### How can we ensure that an effect hook runs only once?
If we pass an empty array [] , it just renders the component only once like componentDidMount .

### Can useState() update more than one state variable at the same time?
- You could combine the state into one state object and then you could do one setState call and there will only be one render. Unlike the setState in class components, the setState returned from useState doesn’t merge objects with existing state, it replaces the object entirely.

### Is useState() synchronous?
useState and setState both are asynchronous. Even though they are asynchronous, the useState and setState functions do not return promises. Therefore we cannot attach a then handler to it or use async/await to get the updated state values.


- State Hook: let you use state and other React features without writing a class with a function component

- Component Lifecycle: These methods are called the component's lifecycle methods and they are invoked in a predictable order. Basically all the React component's lifecyle methods can be split in four phases: initialization, mounting, updating and unmounting.

### Preparation Materials
##### How does useReducer work?
useReducer is used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second.

useReducer is one of the additional Hooks that shipped with React 16.8. An alternative to the useState Hook, it helps you manage complex state logic in React applications. When combined with other Hooks like useContext, useReducer can be a good alternative to Redux or MobX — indeed, it can sometimes be an outright better option.

For those who may be unfamiliar with Redux, we’ll explore this concept a bit further. There are three main building blocks in Redux:

- A store — an immutable object that holds the applications state data
- A reducer — a function that returns some state data, triggered by an action type
- An action — an object that tells the reducer how to change the state. It must contain a type property, and it can contain an optional payload property



