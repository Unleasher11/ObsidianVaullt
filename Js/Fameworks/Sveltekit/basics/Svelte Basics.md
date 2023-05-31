#framework #js #web 

## installation 

> npx degit to copy template file and then point to sveltejs 
> App-name the name the app that you are creating
```node
npx degit sveltejs/template svelte App-name
```

> to install teplate
```node
npm i | npm install
```

>serve locally 
```node 
npm run dev
```



## svelte reactivity
### svelte file template
```html
<!-- the js logic of the component -->
<script lang="ts">
	
</script>

<!-- the style of the component -->
<style>
	
</style>

<!-- the html scleton of the components AKA markup -->
<htmlCode></htmlCode>
```
### js in the Html


```html
<script>
    let local_var = 'local_variable' /** this var is private for this component*/
    export let exported_var = 'exported' /** this var can be used and used from other                components*/
</script>



<div>
<!-- to use this var you can added use {} -->
	{local_var}
	{exported_var}
</div>
```


### the Binding
```html
<script>
    let local_var = 'local_variable' /** this var is private for this component*/
    export let exported_var = 'exported' /** this var can be used and used from other                components*/
    /** function that handle event*/
	function handleEvent(event){
	
	}
</script>


<!--binding onclick event to handleEvent function -->
<div on:click={ handleEvent } >
<!-- to use this var you can added use {} -->
	{local_var}
	{exported_var}
</div>
```


### The $ directive easy way for computed values

```html 
<script>
	/** $: var_name = expression*/
	export let rando;
	$:result = Math.round(rando) ? 'winner' : 'loser'

</script>


<div>
	{result}
	{result}
</div>
```


### the Bind a 2 way relation


```html
<script>
	let inputValue
	/** add export to let the other component access this binded value in case of import this*/
	export let inputValue
</script>

<input type="text" bind:value={inputValue}>
```



### the Conditional logic


```js
{#if expression}
	render
{#/if}

{#if result > 75}
	<p>winner</p>
{:else if result > 50}
	<p> decent</p>
{:else}
	<p>loser</p>
{#/if}

```



### Arrays rendering 
> svelte reacts base on the assiments

```html
<script>
	/**inreactive Array*/
	let randos = [] 
	randos.push('15')
	/** reactive Array with the spread syntax*/
	randos = [...randos, '15'] /** reassine the array  and adding the '15' element*/
	
</script>
```

> the rendering using the eash directive
```js
/**{#eash collection as element ,index } index is async value
	 render_Element
{/eash} */


{#eash randos as val}
	<p> val </p>
{/each}
```



### handling Promeses
```js


/** creating the promise*/
export let name
/** helper function to create a Promise and return it*/
function delay(ms){
	return new Promise(resolve => setTimeout(resolve))
}
/** the promise return a random number after the delay*/
let rando = delay(2000).then(v => Math.random)
```

> the three state of Promises
> waiting 
> resolve
> error

handling the state of the promise in the markup
```js
{#await}
	<p> awaiting promise
{:then number/*the promise result*/}
    <p> resolved with {number}</p>
{:catch error}
	<p> {error.message} </p>
{/awit}
```

## Svelte Stores
> it can be shared anywhere in the components tree
> an easy mechanisim to share data anywhere in the app

>creating a writable store
```js
import { writable } from 'svelte/store'
export const randomStore = writable(Math.random())
/*setting the value using set*/
randomStore.set(new_Value)
/*or using update to get acces to current value and change it
using a call back function */
randomStore.update(v => v+1 )

/* to listen to value all you need is to subscribe to the store
using a callback function*/
randomStore.subscribe()

```
![[Svelte 3 Reaction _ QuickStart Tutorial(1080P_HD).mp4]]