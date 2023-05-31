
React Router is a popular library for handling routing in React applications. It allows you to navigate between different pages or views without the need for a full page reload. Here's an introduction to React Router with three examples:

1. Basic Routing:

```jsx
import React from 'react';
import { BrowserRouter as Router, Switch, Route, Link } from 'react-router-dom';

function Home() {
  return <h2>Home</h2>;
}

function About() {
  return <h2>About</h2>;
}

function Contact() {
  return <h2>Contact</h2>;
}

function App() {
  return (
    <Router>
      <div>
        <nav>
          <ul>
            <li>
              <Link to="/">Home</Link>
            </li>
            <li>
              <Link to="/about">About</Link>
            </li>
            <li>
              <Link to="/contact">Contact</Link>
            </li>
          </ul>
        </nav>

        <Switch>
          <Route path="/about">
            <About />
          </Route>
          <Route path="/contact">
            <Contact />
          </Route>
          <Route path="/">
            <Home />
          </Route>
        </Switch>
      </div>
    </Router>
  );
}
```

In this example, the `Router` component from React Router is used to provide routing functionality to the app. The `Link` component is used to define navigation links. The `Switch` component is used to render only the first `Route` that matches the current URL. Each `Route` component is associated with a specific path and renders the corresponding component when that path is matched.

2. Route Parameters:

```jsx
import React from 'react';
import { BrowserRouter as Router, Switch, Route, Link, useParams } from 'react-router-dom';

function User() {
  const { username } = useParams();

  return <h2>User: {username}</h2>;
}

function App() {
  return (
    <Router>
      <div>
        <nav>
          <ul>
            <li>
              <Link to="/user/john">John</Link>
            </li>
            <li>
              <Link to="/user/jane">Jane</Link>
            </li>
          </ul>
        </nav>

        <Switch>
          <Route path="/user/:username">
            <User />
          </Route>
        </Switch>
      </div>
    </Router>
  );
}
```

In this example, the `:username` in the `path` prop of the `Route` component is a route parameter that captures the dynamic part of the URL. The `useParams` hook is used in the `User` component to access the value of the `:username` parameter. This allows us to render different content based on the username in the URL.

3. Nested Routing:

```jsx
import React from 'react';
import { BrowserRouter as Router, Switch, Route, Link } from 'react-router-dom';

function Home() {
  return <h2>Home</h2>;
}

function Products() {
  return (
    <div>
      <h2>Products</h2>
      <ul>
        <li>
          <Link to="/products/1">Product 1</Link>
        </li>
        <li>
          <Link to="/products/2">Product 2</Link>
        </li>
      </ul>

      <Switch>
        <Route path="/products/:productId">
          <ProductDetails />
        </Route>
      </Switch>
    </div>
  );
}

function ProductDetails() {
  const { productId } = useParams();

  return <h

3>Product Details: {productId}</h3>;
}

function App() {
  return (
    <Router>
      <div>
        <nav>
          <ul>
            <li>
              <Link to="/">Home</Link>
            </li>
            <li>
              <Link to="/products">Products</Link>
            </li>
          </ul>
        </nav>

        <Switch>
          <Route path="/products">
            <Products />
          </Route>
          <Route path="/">
            <Home />
          </Route>
        </Switch>
      </div>
    </Router>
  );
}
```

In this example, the `Products` component is nested within the `Home` component. The `Products` component contains its own set of routes. When a product is clicked, the `ProductDetails` component is rendered with the corresponding `productId` route parameter.

These examples demonstrate how to use React Router to handle routing in a React application. React Router provides various components and hooks to facilitate routing, including `Router`, `Switch`, `Route`, `Link`, and `useParams`. It allows you to create dynamic and navigable applications with multiple views.