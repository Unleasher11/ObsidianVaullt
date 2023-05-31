
Conditional rendering in React allows you to display different content or components based on certain conditions. Here are three examples of conditional rendering in React:

1. Rendering based on a boolean condition:

```jsx
import React from 'react';

function Greeting({ isLoggedIn }) {
  if (isLoggedIn) {
    return <h2>Welcome back!</h2>;
  } else {
    return <h2>Please log in.</h2>;
  }
}

function App() {
  const isLoggedIn = true;

  return (
    <div>
      <h1>Conditional Rendering Example</h1>
      <Greeting isLoggedIn={isLoggedIn} />
    </div>
  );
}
```

In this example, the `Greeting` component displays different greetings based on the `isLoggedIn` prop. If `isLoggedIn` is `true`, it renders "Welcome back!" as an `h2` element. Otherwise, it renders "Please log in." as an `h2` element.

2. Rendering based on an array of data:

```jsx
import React from 'react';

function ItemList({ items }) {
  if (items.length === 0) {
    return <p>No items available.</p>;
  } else {
    return (
      <ul>
        {items.map((item, index) => (
          <li key={index}>{item}</li>
        ))}
      </ul>
    );
  }
}

function App() {
  const items = ['Apple', 'Banana', 'Orange'];

  return (
    <div>
      <h1>Conditional Rendering Example</h1>
      <ItemList items={items} />
    </div>
  );
}
```

In this example, the `ItemList` component renders an unordered list (`ul`) with items from the `items` prop. If the `items` array is empty, it displays "No items available." as a `p` element. Otherwise, it maps over the `items` array and renders each item as a list item (`li`).

3. Rendering based on a switch statement:

```jsx
import React from 'react';

function UserStatus({ status }) {
  switch (status) {
    case 'active':
      return <p>User is active.</p>;
    case 'inactive':
      return <p>User is inactive.</p>;
    case 'pending':
      return <p>User is pending approval.</p>;
    default:
      return null;
  }
}

function App() {
  const userStatus = 'active';

  return (
    <div>
      <h1>Conditional Rendering Example</h1>
      <UserStatus status={userStatus} />
    </div>
  );
}
```

In this example, the `UserStatus` component renders different messages based on the `status` prop. It uses a `switch` statement to check the value of `status` and renders a corresponding message. If the `status` value doesn't match any of the cases, it returns `null`.

These examples demonstrate how to conditionally render content or components in React based on various conditions such as boolean values, array lengths, or switch cases. Conditional rendering allows you to create dynamic and personalized UIs based on different states and data.