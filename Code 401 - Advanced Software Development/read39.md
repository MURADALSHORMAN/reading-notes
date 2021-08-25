# Redux - Additional Topics
# Review, Research, and Discussion
* What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?

The most ‘redux-like’ way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app.

* When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

You export the actual action from the reducer.

## Document the following Vocabulary Terms
* middleware Redux middleware is a snippet of code that provides a third-party extension point between dispatching an action and the moment it reaches the reducers.

* thunk The thunk middleware allows us to write functions that get dispatch and getState as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.


## Redux Toolkit includes these APIs:
* configureStore()
* createReducer()
* createAction()
* createSlice()
* createAsyncThunk












