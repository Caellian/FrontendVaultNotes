React provides little means for handling global state, responsibility for state management is delegated to libraries such as [[Redux]] which often provide a lot of other additional benefits such as time-travel, atomicity, and removing a lot of boilerplate code from the codebase (e.g. `StateManager`, synchronization primitives, ...).

- #hook [const [state, setState] = useState(initial)](https://beta.reactjs.org/reference/react/useState) - declare a state constant

- #api [createContext(defaultValue)](https://beta.reactjs.org/reference/react/createContext) - create a context that components can provide or read
	- Creates a **Context** with a `Provider` field 
	- **Context** also has a `Consumer` field, but `useContext(Context)` does the same and transpiles faster
- #hook [useContext(Context)](https://beta.reactjs.org/reference/react/useContext) - read and subscribe to [context](https://beta.reactjs.org/learn/passing-data-deeply-with-context) from your component
	- allows passing data deeply into the component tree structure
	- doesn't consider providers from the same level, only upwards

- #hook [useSyncExternalStore(subscribe, getSnapshot, getServerSnapshot?)
](https://beta.reactjs.org/reference/react/useSyncExternalStore) - subscribe to an external store
	- `subscribe` - takes a single `callback` argument and subscribes it to the store
	- `getSnapshot` - return snapshot of the data in the store that's needed by the component
		- causes re-renders on change (detected via `Object.is`) 
	- `getServerSnapshot` - initial data used by SSR


