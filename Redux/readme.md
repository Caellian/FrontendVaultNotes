- [How Redux works internally](https://blog.isquaredsoftware.com/2018/11/react-redux-history-implementation/)

## Hooks
- `useSelector((state) => access)` - reads a value from the store state and subscribes to updates
	- e.g. `useSelector((state) => state.counter.value)`
- `const dispatch = useDispatch()` - returns the store's `dispatch` method to allow dispatching actions
	- Used as `dispatch(<dispatchMethodCall>)
		- e.g. `onClick={() => dispatch(decrement())}`

## API
- `createSlice({name, initialState, reducers})` - create a slice
	- A slice is a small part of application state, that _can_ be mutated
- `createStore({reducers, preloadedState?, enchancer?})` - create a store
	- use `compose(...fns)` from Redux to join multiple enhancers into one
- `createReducer(<reducerFn>)` -  takes a function and returns a Redux reducer
- `combineReducers({name: reducer, ...})` - combines multiple reducers that handle different actions
- `applyMiddleware(...middleware)` - adds Rexus middleware API function

## Integrating Redux with a UI
1.  Create a Redux store
2.  Subscribe to updates
3.  Inside the subscription callback:
    1.  Get the current store state
    2.  Extract the data needed by this piece of UI
    3.  Update the UI with the data
4.  If necessary, render the UI with initial state
5.  Respond to UI inputs by dispatching Redux actions
