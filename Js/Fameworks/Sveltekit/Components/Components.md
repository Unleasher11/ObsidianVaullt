
Components in SvelteKit allow you to build reusable and self-contained UI elements. They encapsulate HTML, CSS, and JavaScript logic, making it easy to create modular and maintainable code. Here's an introduction to components in SvelteKit along with three examples:

1. **Basic Component**:
A basic component in SvelteKit consists of a `.svelte` file that contains the markup, style, and logic for the component. Here's an example of a simple button component:

```html
<!-- Button.svelte -->
<script>
  export let text;
</script>

<button>{text}</button>

<style>
  button {
    padding: 10px 20px;
    background-color: #3498db;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
</style>
```

You can use this button component in other parts of your application by importing and using it like this:

```html
<!-- App.svelte -->
<script>
  import Button from './Button.svelte';
</script>

<Button text="Click me" />
```

In the above example, the `Button` component accepts a `text` prop that determines the text displayed on the button. This prop is passed from the parent component (`App.svelte`) and rendered inside the button element.

2. **Nested Components**:
SvelteKit allows you to nest components within each other to create more complex UI structures. Here's an example of a parent component (`Card.svelte`) that contains a nested child component (`Button.svelte`):

```html
<!-- Card.svelte -->
<script>
  import Button from './Button.svelte';
</script>

<div class="card">
  <h2>Title</h2>
  <p>Some content here</p>
  <Button text="Click me" />
</div>

<style>
  .card {
    border: 1px solid #ccc;
    padding: 20px;
    border-radius: 4px;
  }
</style>
```

In the above example, the `Card` component contains a `Button` component, which can be used to perform actions specific to the card. This allows for modular composition of components.

3. **Dynamic Components**:
SvelteKit allows you to conditionally render components based on certain conditions or data. Here's an example where we render different components based on a `type` prop:

```html
<!-- DynamicComponent.svelte -->
<script>
  import Button from './Button.svelte';

  export let type;
</script>

{#if type === 'button'}
  <Button text="Click me" />
{:else if type === 'input'}
  <input type="text" placeholder="Enter something" />
{:else}
  <p>Invalid type</p>
{/if}
```

In the above example, the `DynamicComponent` component receives a `type` prop. Based on the value of `type`, it renders a different component. In this case, it renders a `Button` component if the `type` is `'button'`, an `input` element if the `type` is `'input'`, and a paragraph element with an error message for any other value.

These examples showcase the flexibility and reusability of components in SvelteKit. You can create complex UI structures by nesting components, pass data through props, and dynamically render components based on conditions. Components are a core building block in SvelteKit, helping you create modular and maintainable web applications.