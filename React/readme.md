## Commands
```sh
npx create-react-app <path>
```

## Components

### Fragment
```jsx
<>
	<OneChild />
	<AnotherChild />
</>
```

### Profiler
Measure rendering performance of a React tree programmatically
```jsx
<Profiler id="App" onRender={onRender}>
	<App />
</Profiler>
```

### StrictMode
Helpful for finding common bugs in components in development environment.

```jsx
<StrictMode>
	<App />
</StrictMode>
```

### Suspense

Displays a fallback until its children have finished loading.

```jsx
<Suspense fallback={<Loading />}>
  <SomeComponent />
</Suspense>
```

## Hooks

-   [useCallback](https://beta.reactjs.org/reference/react/useCallback) - cache a function definition between re-renders
-   [useContext](https://beta.reactjs.org/reference/react/useContext) - read and subscribe to [context](https://beta.reactjs.org/learn/passing-data-deeply-with-context) from your component
-   [useDebugValue](https://beta.reactjs.org/reference/react/useDebugValue) - add a label to a custom Hook in React DevTools
-   [useDeferredValue(value)](https://beta.reactjs.org/reference/react/useDeferredValue) - defer updating UI on property change
	- UI first renders with the old value, then it updates again in the background with the new value
-   [useId](https://beta.reactjs.org/reference/react/useId) - generates unique IDs that can be passed to accessibility attributes
-   [useImperativeHandle(ref, createHandle, dependencies?)](https://beta.reactjs.org/reference/react/useImperativeHandle) - customize the handle exposed as a ref

-   [useEffect(setup, dependencies?)](https://beta.reactjs.org/reference/react/useEffect) - used for connecting to external systems (i.e. "stepping outside of React")
-   [useLayoutEffect](https://beta.reactjs.org/reference/react/useLayoutEffect) - fires before re-painting; used for layouts
-   [useInsertionEffect](https://beta.reactjs.org/reference/react/useInsertionEffect)  - fires before any DOM mutations; used for configuring CSS props

-   [const cachedValue = useMemo(calculateValue, dependencies)](https://beta.reactjs.org/reference/react/useMemo) - cache the result of a calculation between re-renders
-   [const [state, dispatch] = useReducer(reducer, initialArg, init?)](https://beta.reactjs.org/reference/react/useReducer)
-   [useRef](https://beta.reactjs.org/reference/react/useRef) - declare a mutable (not used in UI) reference
-   [const [state, setState] = useState(initial)](https://beta.reactjs.org/reference/react/useState) - declare a state constant
-   [useSyncExternalStore](https://beta.reactjs.org/reference/react/useSyncExternalStore) - subscribe to an external store
-   [useTransition](https://beta.reactjs.org/reference/react/useTransition) - used for creating `[is<Action>, start<Action>]`

## API
-   [createContext](https://beta.reactjs.org/reference/react/createContext) - create a context that components can provide or read
-   [forwardRef](https://beta.reactjs.org/reference/react/forwardRef) - expose a DOM node to parent component with a [ref](https://beta.reactjs.org/learn/manipulating-the-dom-with-refs).
-   [lazy](https://beta.reactjs.org/reference/react/lazy) - defer loading component’s code until it is rendered for the first time
-   [memo](https://beta.reactjs.org/reference/react/memo) - skip re-rendering a component when its props are unchanged
-   [startTransition](https://beta.reactjs.org/reference/react/startTransition) - update the state without blocking the UI
