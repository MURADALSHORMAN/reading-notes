## Describe use cases useState() vs useReducer()
* useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.
* Although useState is a Basic Hook for managing simple state transformation and useReducer is an Additional Hook for managing more complex state logic, it is worth noting that useState uses the useReducer internally. This implies that you could use useReducer for everything you can do with useState.
* useReducer lets you avoid passing down callbacks through different levels of your component, instead allowing you to pass a provided dispatch function, which in turn will improve performance for components that trigger deep updates.
* the useState updater function is newly called on each render. What it means is that when you have a complex logic to update state, you simply won’t use the setter directly to update state; instead, you will write a complex function, which in turn would call the setter with updated state.


## Review, Research, and Discussion
### Describe use cases useState() vs useReducer()

 useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

* Why do custom hooks need the use prefix?


Custom hooks are normal JS functions, named with the prefix ‘use’, that can use hooks inside of it and contain a common stateful logic to be reused in other components.

* What do custom hooks usually do?

Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks.

* Using any list of custom hooks, research and name one that you think will be useful in your applications

useScript React hook to dynamically load an external script and know when its loaded

1- useScript is a hook for loading (and notifying when they’re loaded) external scripts, dynamically.

2- use-mouse-action

A library with three React hooks for listening to mouse events on an element or JSX element. useMouseAction: This is used to register mouse actions on an element. useMouseDown: This is used to register a mouse down event on an element. useMouseUp: This registers a mouse up event on an element.


### reducer:
The concept of a Reducer became popular in JavaScript with the rise of Redux as state management solution for React. Basically reducers are there to manage state in an application. For instance, if a user writes something in an HTML input field, the application has to manage this UI state (e.g. controlled components)

### Context
In a typical React application, data is passed top-down (parent to child) via props, but such usage can be cumbersome for certain types of props (e.g. locale preference, UI theme) that are required by many components within an application

### Globally Accessible
The state of our snackbars (which ones are visible) can be localized to a single centralized component. That same centralized component can be responsible for rendering them. There’s really no need for another component somewhere in the tree to hook into that state (at least not in our use-case)

### Room for Change
There’s a lot of buzz around how you can replace a lot of what Redux does with useContext and useReducer. The combination of these two hooks means we can have a global state and use Redux-like reducers, actions, and dispatchers to mutate that global state














