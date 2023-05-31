In earlier versions of React (before React 16.3), class components had lifecycle methods that allowed developers to perform certain actions at specific points in the component's lifecycle. However, with the introduction of React hooks, the use of lifecycle methods has been minimized. Nonetheless, here's an introduction to three common lifecycle methods with examples:

1. componentDidMount():

The `componentDidMount()` method is invoked immediately after a component is mounted (inserted into the DOM tree). It is commonly used to perform initial setup, data fetching, or subscriptions.

```jsx
import React from 'react';

class MyComponent extends React.Component {
  componentDidMount() {
    console.log('Component mounted');
    // Perform additional setup or fetch data here
  }

  render() {
    return <h1>Hello, World!</h1>;
  }
}
```

In this example, the `componentDidMount()` method is used to log a message to the console when the component is mounted. You can perform additional setup tasks or fetch data from APIs in this method.

2. componentDidUpdate():

The `componentDidUpdate()` method is called after a component has been updated and re-rendered. It is commonly used to respond to changes in props or state and perform side effects based on those changes.

```jsx
import React from 'react';

class MyComponent extends React.Component {
  componentDidUpdate(prevProps, prevState) {
    if (this.props.count !== prevProps.count) {
      console.log('Count prop changed');
      // Perform additional actions based on prop change
    }
  }

  render() {
    return <h1>{this.props.count}</h1>;
  }
}
```

In this example, the `componentDidUpdate()` method is used to check if the `count` prop has changed. If it has, a message is logged to the console. You can perform additional actions based on prop or state changes in this method.

3. componentWillUnmount():

The `componentWillUnmount()` method is invoked just before a component is unmounted and removed from the DOM tree. It is typically used to clean up resources, event listeners, or subscriptions created in the `componentDidMount()` method.

```jsx
import React from 'react';

class MyComponent extends React.Component {
  componentDidMount() {
    console.log('Component mounted');
    document.addEventListener('click', this.handleClick);
  }

  componentWillUnmount() {
    console.log('Component unmounted');
    document.removeEventListener('click', this.handleClick);
  }

  handleClick() {
    // Handle click event
  }

  render() {
    return <h1>Hello, World!</h1>;
  }
}
```

In this example, the `componentWillUnmount()` method is used to remove an event listener (`handleClick()`) that was added in the `componentDidMount()` method. This ensures that the event listener is properly cleaned up when the component is unmounted, preventing memory leaks.

Note: As of React 16.3, some lifecycle methods have been deprecated and new lifecycle methods have been introduced. The examples provided here are based on the traditional lifecycle methods, but it's recommended to use hooks like `useEffect()` for handling side effects and cleanup in functional components.

With the introduction of hooks, the useEffect() hook can handle component lifecycle behavior in a more flexible and unified way.