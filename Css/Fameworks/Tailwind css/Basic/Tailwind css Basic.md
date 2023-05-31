#framework #css #web 

# installation
> go the documention for every case

> the comment steps 
> go the index.css and add 

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```


# the tailwind config file
>content initially
```js
module.exports ={
	mode:'jit', // just in time mode
	purge:['.exmaple regex'], // purging any unused css in the bundle
	darkMode:fase,
	theme:{
		extend:{}
	},
	variants:{
		extend:{},
	},
	plugins:[]
}
```


# the main flow of using tailwind css
> class utilities
> tailwind css is a collection of classes that you use together to create the UI that you want !



![[Ultimate Tailwind CSS Tutorial __ Build a Discord-inspired Animated Navbar(720P_HD).mp4]]