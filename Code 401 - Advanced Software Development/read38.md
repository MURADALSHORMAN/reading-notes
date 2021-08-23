# Redux - Asynchronous Actions
## Review, Research, and Discussion
* How granular should your reducers be?

 It is difficult to manage states that are deeply nested, so more reducers is better than only a few. Redux gives us combineReducers to let us define more precisely what our initial state will look like.

* Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

 Con as it gets messy and actions need to get filtered through.

* Name a strategy for preventing the above

 Using Redux middleware thunk, allows for evaluating the actions.


# Preparation Materials
* Async Logic and Data Fetching *React-Redux library let our React components interact with a Redux store, including calling useSelector to read Redux state, calling useDispatch to give us access to the dispatch function, and wrapping our app in a component to give those hooks access to the store.*

So far, all the data we’ve worked with has been directly inside of our React+Redux client application. However, most real applications need to work with data from a server, by making HTTP API calls to fetch and save items.

* Redux Middleware and Side Effects By itself, a Redux store doesn’t know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

#  Vocabulary Terms
* store: is a state container which holds the application’s state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer. Let us see how we can create a store using the createStore method from Redux.
* combined reducers: a helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore . The resulting reducer calls every child reducer, and gathers their results into a single state object.


