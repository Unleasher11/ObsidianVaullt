
Hooks are a feature introduced in React 16.8 that allow you to use state and other React features in functional components. They provide a way to reuse stateful logic, manage side effects, and enhance the functionality of functional components. Here's an introduction to three commonly used hooks in React with examples:

1. useState():

The `useState()` hook allows functional components to have local state. It takes an initial state value as an argument and returns an array with two elements: the current state value and a function to update the state.

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <h2>Count: {count}</h2>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
```

In this example, the `useState()` hook is used to add local state to the `Counter` component. The `count` variable holds the current state value, and the `setCount` function is used to update the state. When the button is clicked, the `increment` function is called, which increments the count by 1 using the `setCount` function.

2. useEffect():

The `useEffect()` hook is used to perform side effects in functional components. It allows you to run code in response to component updates, such as fetching data, subscribing to events, or cleaning up resources.

```jsx
import React, { useState, useEffect } from 'react';

function DataFetcher() {
  const [data, setData] = useState(null);

  useEffect(() => {
    // Fetch data from API
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => setData(data));

    // Cleanup function (optional)
    return () => {
      // Cleanup code (unsubscribe, remove event listeners, etc.)
    };
  }, []);

  return (
    <div>
      {data ? (
        <h2>Data: {data}</h2>
      ) : (
        <p>Loading data...</p>
      )}
    </div>
  );
}
```

In this example, the `useEffect()` hook is used to fetch data from an API when the component mounts. The empty dependency array `[]` as the second argument ensures that the effect runs only once, similar to `componentDidMount()`. The fetched data is stored in the `data` state variable using the `setData` function. The cleanup function (returned by `useEffect`) is used to unsubscribe or perform any necessary cleanup tasks when the component is unmounted or when the effect is re-run.

3. useContext():

The `useContext()` hook enables functional components to consume values from a React context. It allows you to access context values without using a `Consumer` component.

```jsx
import React, { useContext } from 'react';

const ThemeContext = React.createContext('light');

function ThemeDisplay() {
  const theme = useContext(ThemeContext);

  return (
    <div>
      <h2>Current Theme: {theme}</h2>
    </div>
  );
}

function App() {
  return (
    <ThemeContext.Provider value="dark">
      <ThemeDisplay />
    </ThemeContext.Provider>
  );
}
```

In this example, the `useContext()` hook is used to access the current theme value from the `ThemeContext`. The `ThemeDisplay` component consumes the value of the `ThemeContext` and renders the current theme. The `App` component provides the theme value of "dark" to the `ThemeContext` using the `Provider`

 component.

These are just a few examples of hooks in React. React provides several other built-in hooks like `useReducer()`, `useCallback()`, and `useMemo()`, as well as the ability to create custom hooks. Hooks allow functional components to have similar capabilities as class components and make it easier to manage state and side effects in a more concise and readable way.