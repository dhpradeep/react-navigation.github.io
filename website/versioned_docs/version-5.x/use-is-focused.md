---
id: version-5.x-use-is-focused
title: useIsFocused
sidebar_label: useIsFocused
original_id: use-is-focused
---

We might want to render different content based on the current focus state of the screen. The library exports a `useIsFocused` hook to make this easier:

<samp id="use-is-focused">

```js
import { useIsFocused } from '@react-navigation/native';

// ...

function Profile() {
  const isFocused = useIsFocused();

  return <Text>{isFocused ? 'focused' : 'unfocused'}</Text>;
}
```

Note that using this hook triggers a re-render for the screen when it changes focus. This might cause lags during the animation if your screen is heavy. You might want to extract the expensive parts to separate components and use [`React.memo`](https://reactjs.org/docs/react-api.html#reactmemo) or [`React.PureComponent`](https://reactjs.org/docs/react-api.html#reactpurecomponent) to minimize re-renders for them.
