Transitions are used to smoothly animate changes between CSS styles when a component enters or leaves the DOM. They're used for simple animations like fading in/out, sliding up/down, etc.

Transitions are very similar to [Effects](Effects.md) but be used to animate changes to a component styles.

## Related hooks & API

- #hook [const [isPending, startTransition] = useTransition()](https://beta.reactjs.org/reference/react/useTransition) - modify state without blocking the on the main/UI/render thread
	- `startTransition` takes a single `scope` function which is meant to mutate state provided by `useState()` 
- #api [startTransition(scope)](https://beta.reactjs.org/reference/react/startTransition) - mark a state update as a transition (without block the UI thread)
	- function that updates some state by calling one or more [`set` functions](https://beta.reactjs.org/reference/react/useState#setstate).
	- [hides loading indicators](https://beta.reactjs.org/reference/react/useTransition#preventing-unwanted-loading-indicators).