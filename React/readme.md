## Commands
```sh
# init a React project
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

-   [useCallback(fn, dependencies)](https://beta.reactjs.org/reference/react/useCallback) - cache a function definition between re-renders
	- when `dependencies` update, the definition gets updated, it's cached otherwise
-   [useContext(Context)](https://beta.reactjs.org/reference/react/useContext) - read and subscribe to [context](https://beta.reactjs.org/learn/passing-data-deeply-with-context) from your component
	- allows passing data deeply into the component tree structure
	- doesn't consider providers from the same level, only upwards
-   [useDebugValue(value, format?)](https://beta.reactjs.org/reference/react/useDebugValue) - add a label to a custom Hook in React DevTools
-   [useDeferredValue(value)](https://beta.reactjs.org/reference/react/useDeferredValue) - show stale content while fresh content is still loading
	- UI first renders with the old value, then it updates again in the background with the new value
-   [useId()](https://beta.reactjs.org/reference/react/useId) - generates unique IDs that can be passed to accessibility attributes
	- e.g. `aria-describedby={passwordHintId}`
-   [useImperativeHandle(ref, createHandle, dependencies?)](https://beta.reactjs.org/reference/react/useImperativeHandle) - customize the handle exposed as a ref
-   [const cachedValue = useMemo(calculateValue, dependencies)](https://beta.reactjs.org/reference/react/useMemo) - cache the result of a calculation between re-renders
-   [const [state, dispatch] = useReducer(reducer, initialArg, init?)](https://beta.reactjs.org/reference/react/useReducer)
-   [useRef(initialValue)](https://beta.reactjs.org/reference/react/useRef) - declare a mutable reference for values not needed for rendering
	- returns a reference with `current` that's set to `initialValue` and can be mutated
-   [const [state, setState] = useState(initial)](https://beta.reactjs.org/reference/react/useState) - declare a state constant
-   [useSyncExternalStore(subscribe, getSnapshot, getServerSnapshot?)
](https://beta.reactjs.org/reference/react/useSyncExternalStore) - subscribe to an external store
	- `subscribe` - takes a single `callback` argument and subscribes it to the store
	- `getSnapshot` - return snapshot of the data in the store that's needed by the component
		- causes re-renders on change (detected via `Object.is`) 
	- `getServerSnapshot` - initial data used by SSR

## API
-   [createContext(defaultValue)](https://beta.reactjs.org/reference/react/createContext) - create a context that components can provide or read
	- Creates a **Context** with a `Provider` field 
	- **Context** also has a `Consumer` field, but `useContext(Context)` does the same and transpiles faster
-   [forwardRef(render)](https://beta.reactjs.org/reference/react/forwardRef) - expose a DOM node to parent component with a [[Refs|ref]]
	- takes a component render function as an argument
-   [lazy(load)](https://beta.reactjs.org/reference/react/lazy) - defer loading component’s code until it is rendered for the first time
	- `const MarkdownPreview = lazy(() => import('./MarkdownPreview.js'));`
-   [memo(Component, arePropsEqual?)](https://beta.reactjs.org/reference/react/memo) - skip re-rendering a component when its props are unchanged
	- `arePropsEqual` allows using custom logic for checking changes
