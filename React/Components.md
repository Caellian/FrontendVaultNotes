## `react` components

### Fragment

Used for returning multiple components from a single render function.

The returned content won't be wrapped within a component in DOM. That in turn allows some nifty logic handling like factoring out table rows from a `Table` component.

```jsx
<>
	<OneChild />
	<AnotherChild />
</>
```

### Profiler

Measures rendering performance of a React tree programmatically. Shouldn't be left in production environment.

```jsx
<Profiler id="App" onRender={onRender}>
	<App />
</Profiler>
```

### StrictMode
Helpful for finding common bugs in components in development environment. Primarily intended for development environment, shouldn't be left in production environment.

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

## Related hooks & API

- #hook [const [state, dispatch] = useReducer(reducer, initialArg, init?)](https://beta.reactjs.org/reference/react/useReducer) - allows adding [reducer](https://beta.reactjs.org/learn/extracting-state-logic-into-a-reducer) to components