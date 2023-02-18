A _pure_ function that takes the existing state and actions and returns the new state.
$R(State, Action) \rightarrow State_{New}$

To create a single Redux reducer from a reducer function $R$, use `createReducer(R)`.

Slices have _multiple_ actions, they contain one reducer (`slice.reducer`) that handles all action mutations.