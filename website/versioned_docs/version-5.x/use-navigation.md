---
id: version-5.x-use-navigation
title: useNavigation
sidebar_label: useNavigation
original_id: use-navigation
---

`useNavigation` is a hook which gives access to `navigation` object. It's useful when you cannot pass the `navigation` prop into the component directly, or don't want to pass it in case of a deeply nested child.

`useNavigation()` returns the `navigation` prop of the screen it's inside.

## Example

<samp id="use-navigation-example">

```js
import * as React from 'react';
import { Button } from 'react-native';
import { useNavigation } from '@react-navigation/native';

function MyBackButton() {
  const navigation = useNavigation();

  return (
    <Button
      title="Back"
      onPress={() => {
        navigation.goBack();
      }}
    />
  );
}
```

See the documentation for the [`navigation` prop](navigation-prop.html) for more info.
