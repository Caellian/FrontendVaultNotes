Only use refs for _imperative_ behaviors that you can’t express as props: for example, scrolling to a node, focusing a node, triggering an animation, selecting text, and so on.

**I something can be expressed as a prop, it should be preffered over using a ref.**

[[Effects]] can help exposing imperative behaviors via props.
