
In React, props (short for "properties") are used to pass data from a parent component to its child components. Props allow you to customize the behavior and appearance of child components based on the data provided by their parent. Here's an introduction to props in React with three examples:

1. Passing Data as Props:

Parent Component:
```jsx
import React from 'react';
import ChildComponent from './ChildComponent';

function ParentComponent() {
  const name = 'John';
  const age = 30;

  return (
    <div>
      <h2>Parent Component</h2>
      <ChildComponent name={name} age={age} />
    </div>
  );
}

export default ParentComponent;
```

Child Component:
```jsx
import React from 'react';

function ChildComponent(props) {
  return (
    <div>
      <h3>Child Component</h3>
      <p>Name: {props.name}</p>
      <p>Age: {props.age}</p>
    </div>
  );
}

export default ChildComponent;
```

In this example, the `ParentComponent` renders the `ChildComponent` and passes data as props. The `name` and `age` variables in the parent component are passed to the child component using attributes (`name={name}` and `age={age}`). In the child component, the data is accessed through the `props` object.

2. Passing Functions as Props:

Parent Component:
```jsx
import React from 'react';
import ChildComponent from './ChildComponent';

function ParentComponent() {
  const handleClick = () => {
    console.log('Button clicked!');
  };

  return (
    <div>
      <h2>Parent Component</h2>
      <ChildComponent handleClick={handleClick} />
    </div>
  );
}

export default ParentComponent;
```

Child Component:
```jsx
import React from 'react';

function ChildComponent(props) {
  return (
    <div>
      <h3>Child Component</h3>
      <button onClick={props.handleClick}>Click me</button>
    </div>
  );
}

export default ChildComponent;
```

In this example, the `ParentComponent` defines a function `handleClick` and passes it as a prop to the `ChildComponent`. The child component uses the `onClick` event handler and invokes the function received through props (`props.handleClick`) when the button is clicked.

3. Conditional Rendering based on Props:

Parent Component:
```jsx
import React from 'react';
import ChildComponent from './ChildComponent';

function ParentComponent() {
  const isLoggedIn = true;

  return (
    <div>
      <h2>Parent Component</h2>
      <ChildComponent isLoggedIn={isLoggedIn} />
    </div>
  );
}

export default ParentComponent;
```

Child Component:
```jsx
import React from 'react';

function ChildComponent(props) {
  return (
    <div>
      <h3>Child Component</h3>
      {props.isLoggedIn ? (
        <p>Welcome, user!</p>
      ) : (
        <p>Please log in.</p>
      )}
    </div>
  );
}

export default ChildComponent;
```

In this example, the `ParentComponent` sets the `isLoggedIn` variable to `true` and passes it as a prop to the `ChildComponent`. The child component conditionally renders different content based on the value of the `isLoggedIn` prop. If `isLoggedIn` is `true`, it displays a welcome message, otherwise, it prompts the user to log in.

Props enable communication between components, allowing data and functions to be passed down the component tree. This helps in creating reusable and flexible components that can be easily customized and composed to build

 complex UIs.