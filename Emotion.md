- [Documentation](https://emotion.sh/docs/introduction) 

## React
```jsx
import { css } from '@emotion/react'

const color = 'white'

render(
  <div
    css={css`
      padding: 32px;
      background-color: hotpink;
      font-size: 24px;
      border-radius: 4px;
      &:hover {
        color: ${color};
      }
    `}
  >
    Hover to change color.
  </div>
)
```

### Object notation
```jsx
import { css } from '@emotion/react'

const hotpink = css({
  color: 'hotpink'
})

render(
  <div>
    <p css={hotpink}>This is hotpink</p>
  </div>
)
```