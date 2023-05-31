

In React, handling events is similar to handling events in traditional HTML. You can use event handlers in JSX syntax to respond to user interactions. Here's an introduction to handling events in React with three examples:

1. Handling Click Events:

```jsx
import React from 'react';

function Button() {
  const handleClick = () => {
    console.log('Button clicked!');
  };

  return (
    <button onClick={handleClick}>Click me</button>
  );
}
```

In this example, the `handleClick` function is called when the button is clicked. It logs a message to the console. The `onClick` attribute in JSX is used to assign the `handleClick` function as the event handler for the button's click event.

2. Handling Form Submission:

```jsx
import React, { useState } from 'react';

function LoginForm() {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log('Username:', username);
    console.log('Password:', password);
    // Perform form submission logic here
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        value={username}
        onChange={(event) => setUsername(event.target.value)}
        placeholder="Username"
      />
      <input
        type="password"
        value={password}
        onChange={(event) => setPassword(event.target.value)}
        placeholder="Password"
      />
      <button type="submit">Submit</button>
    </form>
  );
}
```

In this example, the `handleSubmit` function is called when the form is submitted. It prevents the default form submission behavior using `event.preventDefault()`. The form inputs are controlled components, where their values are stored in the component's state (`username` and `password`). The `onChange` event handlers update the state when the input values change.

3. Handling Mouse Hover Events:

```jsx
import React, { useState } from 'react';

function HoverComponent() {
  const [isHovered, setIsHovered] = useState(false);

  const handleMouseEnter = () => {
    setIsHovered(true);
  };

  const handleMouseLeave = () => {
    setIsHovered(false);
  };

  return (
    <div
      onMouseEnter={handleMouseEnter}
      onMouseLeave={handleMouseLeave}
    >
      {isHovered ? 'Mouse is hovering!' : 'Hover over me'}
    </div>
  );
}
```

In this example, the `isHovered` state variable keeps track of whether the mouse is currently hovering over the component. The `handleMouseEnter` function is called when the mouse enters the component, and it sets `isHovered` to `true`. The `handleMouseLeave` function is called when the mouse leaves the component, and it sets `isHovered` to `false`. The component's content is updated based on the value of `isHovered`.

These examples demonstrate how to handle different types of events in React components. Event handlers are specified as attributes in JSX and assigned to corresponding event names. React provides a wide range of event handling options, including click events, form submission events, keyboard events, and more.