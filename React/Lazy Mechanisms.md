
## Related hooks & API

- #hook [useCallback(fn, dependencies)](https://beta.reactjs.org/reference/react/useCallback) - cache a function definition between re-renders
	- when `dependencies` update, the definition gets updated, it's cached otherwise

- #api [lazy(load)](https://beta.reactjs.org/reference/react/lazy) - defer loading component’s code until it is rendered for the first time
	- `const MarkdownPreview = lazy(() => import('./MarkdownPreview.js'));`
- #hook [useDeferredValue(value)](https://beta.reactjs.org/reference/react/useDeferredValue) - show stale content while fresh content is still loading
	- UI first renders with the old value, then it updates again in the background with the new value

- #api [memo(Component, arePropsEqual?)](https://beta.reactjs.org/reference/react/memo) - skip re-rendering a component when its props are unchanged
	- `arePropsEqual` allows using custom logic for checking changes
- #hook [const cachedValue = useMemo(calculateValue, dependencies)](https://beta.reactjs.org/reference/react/useMemo) - cache the result of a calculation between re-renders
