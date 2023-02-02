Only use refs for _imperative_ behaviors that you can’t express as props: for example, scrolling to a node, focusing a node, triggering an animation, selecting text, and so on.

**I something can be expressed as a prop, it should be preffered over using a ref.**

[[Effects]] can help exposing imperative behaviors via props.

## Related hooks & API

- #hook [useRef(initialValue)](https://beta.reactjs.org/reference/react/useRef) - declare a mutable reference for values not needed for rendering
	- returns a reference with `current` that's set to `initialValue` and can be mutated

- #api [forwardRef(render)](https://beta.reactjs.org/reference/react/forwardRef) - expose a DOM node to parent component with a [[Refs|ref]]
	- takes a component render function as an argument
- #hook [useImperativeHandle(ref, createHandle, dependencies?)](https://beta.reactjs.org/reference/react/useImperativeHandle) - customize the handle exposed as a ref