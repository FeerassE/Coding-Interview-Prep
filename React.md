# React

## Handling Events


## Hooks

Hooks add state to function components.

#### useState

useState is a function that allows us to access state from a function component.
```
import React, { useState } from 'react';

// useState parameter is the initial state
// useState returns a pair: the current state value and a function that lets you update it

const [currentValue, setValue] = useState(0)
```

#### useEffect

useEffect is a function that allows us to perform side effects on function components. <br>
It tells React that your component needs to do something after render.
I think useEffect is asynchronous.


```
// trigger an effect once
useEffect(() => {
  // do something
}, [])

// trigger an effect on every render (which I believe is whenever a prop changes or event happens)
useEffect(() => {
  // do something
})

// trigger an effect on state change
useEffect(() => {
  // do something
}, [currentValue])

// clean up after an effect
useEffect(() => {    
  ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);    // Specify how to clean up after this effect:
  return function cleanup() {     
      ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);    
    };
});
```
