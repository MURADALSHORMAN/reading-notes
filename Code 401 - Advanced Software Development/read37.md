# Redux - Combined Reducers
 1. Why choose Redux instead of the Context API for global state?
* Context API is great for small applications where state changes are minimal but Redux is better for large applications where there are many changes to state. Redux also offer time-travel and single source of truth for state.

* To manage huge applications with complex state management, in a large scale application, Redux is a better way to control state.

* In a large scale application, Redux is a better way to control state.

 2. What is the purpose of a reducer?
* The reducer takes a state and an action and returns a new state
3. What does an action contain?
* Object literals that tell the reducer what is being done to the app, and any data required for the update.
4. Why do we need to copy the state in a reducer?
* Reducers are not allowed to modify the existing state, instead they must make immutable updates by copying the existing state and making changes to the copied values.


# Preparation Materials
## Using combineReducers
* Core Concepts: A simple Javascript object containing "slices" of domain-specific data at each top-level key is the most typical state form for a Redux app. Similarly, the most popular method to building reducer logic for that state shape is to use "slice reducer" functions, each with the same (state, action) signature and each in charge of managing all modifications to that slice of state. Multiple slice reducers can respond to the same action, updating their own slice as appropriate, and then combining the changed slices into the new state object.
Because this pattern is so common, Redux provides the combineReducers utility to implement that behavior. It is an example of a higher-order reducer, which takes an object full of slice reducer functions, and returns a new reducer function.

* Defining State Shape
The initial shape and contents of your store's state may be defined in two ways. First, preloadedState can be sent as the second parameter to the createStore method. This is mostly used to populate the store with data that was previously saved somewhere else, such the browser's localStorage. When the state parameter is undefined, the root reducer might also return the original state value. These two techniques are discussed in further depth in Initializing State, however when utilizing combineReducers, there are some extra considerations to keep in mind. combineReducers generates a function that outputs a similar state object with the same keys from an object containing slice reducer functions. If createStore is not given a preloaded state, the naming of the keys in the input slice reducer object will be used to name the keys in the output state object. When utilizing ES6 features like default module exports and object literal shorthands, the relationship between these names isn't always obvious.


# Document the following Vocabulary Terms : 
## Term	 
* immutable state	is state that cannot be changed.
* time travel in redux	the ability to move back and forth among the previous states of an application and view the results in real time
* action creator	is merely a function that returns an action object
* reducer	a function that receives the current state and an action object, decides how to update the state if necessary, and returns the new state
* dispatch	The only way to update the state is to call store.dispatch() and pass in an action object.



