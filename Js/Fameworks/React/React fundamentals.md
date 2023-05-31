#web #framework #js 

>The Fundamentals of React.js include the core concepts and principles that form the foundation of building applications with React. Here are the key fundamentals you should understand:


## Components: 
>eact.js is based on a component-based architecture. Components are reusable, independent, and self-contained building blocks that encapsulate the UI and behavior. There are two types of components: functional components (stateless) and class components (stateful).
>[[Js/Fameworks/React/Components/Components| see more]]

## JSX (JavaScriptXML): 
>JSX is a syntax extension for JavaScript that allows you to write HTML-like code within your JavaScript files. It enables you to define the structure and content of React components in a more declarative manner.
>[[JSX | see more]]

## Virtual DOM: 
>React.js uses a virtual representation of the actual browser Document Object Model (DOM). The virtual DOM is a lightweight copy of the real DOM that React manipulates for efficient rendering and updates. React reconciles the differences between the virtual DOM and the real DOM, updating only the necessary parts of the UI.


## State: 
>State represents the data that changes within a component. Class components have a built-in state object, while functional components can use the useState hook introduced in React 16.8. The state allows components to dynamically update and re-render based on user interactions or other events. [[State | see more]]


## Props (Properties): 
>Props are used to pass data from a parent component to its child components. They are immutable and provide a way to make components more flexible and reusable. Props allow you to customize the behavior and appearance of child components based on the data provided by their parent. [[Props | see more]]


## Lifecycle Methods (Class Components): 
>Class components have lifecycle methods that allow you to perform actions at specific stages of a component's life cycle, such as mounting, updating, and unmounting. Some commonly used lifecycle methods include `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount`.
>[[lifecycle methods | see more]]


## Hooks (Functional Components): 
>Hooks are introduced in React 16.8 as a way to use state and other React features in functional components. They provide a more concise and flexible way to handle component state and lifecycle. Some commonly used hooks include `useState`, `useEffect`, and `useContext`.
>[[Hooks | see more]]


## Conditional Rendering: 
>React allows you to conditionally render components or elements based on certain conditions. You can use conditional statements like `if` or the ternary operator (`?`) to control what gets rendered. [[conditional rendering | see more]]


## Handling Events:
>React provides a synthetic event system that normalizes browser-specific events and provides a consistent interface. You can attach event handlers to components and respond to user interactions such as clicks, input changes, or form submissions.
>[[Handling events | see more]]

## Component Communication: 
>React supports different ways of communication between components. Parent-to-child communication is achieved through props, while child-to-parent communication can be done by passing [[Javascript basic concepts#the call-back function| callback function]] as props. Additionally, React provides techniques like context API, Redux, and React Router for managing state and communication across components.

## React Router: 
>React Router is a popular library that allows you to handle routing in React applications. It enables navigation between different pages or views in a single-page application (SPA) without requiring a full page reload.
>[[Router | see more]]

>These fundamentals form the basis for building React.js applications. It's important to understand and practice these concepts to become proficient in React development. As you gain experience, you can explore more advanced topics and techniques in the React ecosystem.