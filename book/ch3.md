# React Hooks

Ract has 10 builtin hooks :

Basi Hooks 

- useState
- useeffect
- useContext

Additionnal Hooks

- useReducer
- useCallback
- useDemo
- userRef
- useImperativeHandle
- useLayoutEffect
- useDebugValue

We are going to see only two hooks in this chapter, useState and useEffect

Don't ask your self what is a Hook actually just focus on the useState and useEffect which we going to understand with an example

## useState Hook

useState is a sort of variable in the React logic, `useState()` returns an array which we're going to destructurate like we've seen in ch1 with two values, the a reactive value and a setter

Suppose you have this code :

```
import React from 'react';

function App() {
  let count = 0;
  
  const increment = () => {
    count +=1;
  };

  const decrement = () => {
    count -= 1;
  };
  
  return (
   <div>
    <h1>This is the counter</h1>
    <p> counter : {count}</p>
    <button onClick={decrement}>-</button>
    <button onClick={increment}>+</button>
   </div>
   );
}
```

This code will not work in the React logic if you click + or - buttons why ? Because you have to use useState

```
import React, {useState} from 'react';

function App() {
  const [count, setCount] =useState(0);
  
  const increment = () => {
    setCount(count + 1);
  };

  const decrement = () => {
    setCount(count -1);
  };
  
  return (
   <div>
    <h1>This is the counter</h1>
    <p> counter : {count}</p>
    <button onClick={decrement}>-</button>
    <button onClick={increment}>+</button>
   </div>
   );
}
```

useState is called a Hook

