# useState Hook

Don't ask your self what is a Hook a ctually just focus on the useStat wich is a sort of variable in React logic

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

