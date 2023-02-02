Effects are generally used for fetching data from an API, responding to user interactions, or triggering animations. That is for everything besides React.

They can be used for offloading time intensive logic (e.g. caching assets for offline access, intercepting network requests, and receiving push notifications) from the UI thread, but a [service worker](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) still needs to be created.

## Related hooks & API

- #hook [useEffect(setup, dependencies?)](https://beta.reactjs.org/reference/react/useEffect) - used for connecting to external systems (i.e. "stepping outside of React")
- #hook [useLayoutEffect](https://beta.reactjs.org/reference/react/useLayoutEffect) - fires before re-painting; used for layouts
- #hook [useInsertionEffect](https://beta.reactjs.org/reference/react/useInsertionEffect)  - fires before any DOM mutations; used for configuring CSS props
