- [Properties](https://mui.com/system/properties/)

- MUI System [[Component]]s use the `sx` property as replacement for `style` which provides access to `theme`.

### CSS property level accessors
```js
<Box sx={{ height: (theme) => theme.spacing(10) }} />
```

### Global styles
```ts
const style = {
  flexDirection: 'column',
};

export default function App() {
  return <Button sx={style}>Example</Button>;
}
```

### Passthrough  `sx`
```js
function ListHeader({ sx = [], children }) {
  return (
    <ListItem
      sx={[
        {
          width: 'auto',
          textDecoration: 'underline',
        },
        // You cannot spread `sx` directly because `SxProps` (typeof sx) can be an array.
        ...(Array.isArray(sx) ? sx : [sx]),
      ]}
    >
      <FormLabel sx={{ color: 'inherit' }}>{children}</FormLabel>
    </ListItem>
  );
}
```
