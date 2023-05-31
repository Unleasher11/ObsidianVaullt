#js #languageBasic 

## script tag in HTML


```html
<script src="./externalimport_script.js">
    document.write("local script")
</script>
```

## log 

```js 
console.log('logging in js')
```


## defining a viable

> ***let*** most used
> ***var*** hell to use
> js is dynamically typed language
> Primitive Data type built in js
> string 
> number
> bigint
> boolean 
> undefine
> symbol
> null

```js 
let name = 'test'
var message = 'whatever'
```



## the Objects

> any var that is not primitive typed inherent from the object class

```js
let obj = new Object()
```



## the const

```js
const constant = 'test'
```

## Function
> function are objects in js 
> and the let keyword limit the access of the variable to  the block scope

```js 
function fun(){
	let a = 'function'
}
```

> function details 
> params 0..n
> optional return

```js
function fun(param1,...){
	
	return{
	/optional return statement
	}
}
```

> higher order function
> function that take function as arguments or return value

```js
function Arg(){

}
function HO_function(Arg){
	return function {
	}
}
```

>closure
>it is used to encapsulate the data and the logic from the rest of the program

```js
function giveMeClosure(){
	let a = 10
	return function(){
		a++
		return a;
	}
}
```

# this keyword
> contain the reference to the object base on how a function is called
> in the glabal scope : this : window object
> if the same function is attachet to an object it contains the reference to that object

```js
function wtfIsThis(){
	return console.log(this) // window object
}
const person = {
	wtfIsThis : function (){
		console.log(this)	// person object
	}
}
```
# Binding function 

```js
const person = {}
const personFun = wtfIsThis.bind(person)
```


# Arrow function =>

```js
const person = {
	wtfIsThis: () => {
		console.log(this)
	}
}
```

# argument passing
```js 
	function fun(prim,object){
		prim // is passed by value
		object // is passed by reference
	}
```
## control statement IF

```js
if(true){
	execute_this_Block
}
else{
	execute_this_block
}
```


# Object

## defining an Object

>object literal syntax

```js
	const person = {
	}
```
>object constructor
```js
	const person = new Object()
```

> object contain of collection key value pairs colled Properties

```js
	const person = {
		name:'whatever',
		DNA:'whatever',
		
	}
```

> object can inherit props from each other using mechanism called Prototype chain

```js
	human.__proto__.__proto__;
```


# OOP in Js
> oop in js is just syntax sugar for prototype inhertence

```js
class Human{

	static isHuman(human){
		return isInstanceOfThisClass
	}
	constructor(name){
		this.name = name
		this.DNA = 'AAGT'
	}
	get genter(){
		return this.gender
	}
	
	set genter(val){
		 this.gender = val
	}
}
```



# Collection


> Array type : collection of items

```js
	const list = ['foo','bar','bar']
```

> Set type :collection of unique items

```js
	const uniq = new set(list)
```

> Map type : key value pairs collection

```js
	const dict = new Map([
		['foo',1],
		['bar',2]
		])
	const weakdict = new WeakMa([
		['foo',1],
		['bar',2]
	])
```


# the non-blocking event loop

## the call-back function 
```js
	setTimeout(()=>{
		console.log('5 seconds in the future')
	},5000)
```


## the promise
> is a wrapper for a value is unkown right now but will resolve to value in the future 

```js
	const promise = new Promise(
		(resolve, reject) =>{
			//Do something here
			if(greatSuccess){
				resolve('sucess')
			}
			else{
				reject('failure')
			}
		}
	)
	
```

> the consumer of the promise can use then and catch function to hundle the 2 possible outcome 
> of the promise

```js
	promise
			.then( sucess =>{
				console.log('yay',success)
			})
			.catch(err => {console.log('fuck')})
```

## Async function 
> a function that automatically return a promise

```js
		async function asyncFun(){
			const result = await promise // use the await keyword to pose execution 
			}
```

> to handle error use the try catch 

```js
	async function asyncFunction(){
		try{
			const result = await promise
		}catch(error){
			handleError()
		}
	}
```



# Modules
> every js file is called module and every code in the module is privite to this module 


> the export keyword let the usage of the code from the module in other possible 

```js
		export default code // for single exportation 
		export code // for multiple export 
		export code 
```

> to use the exported code in other modules use the import key word

```js
		import Code from 'module.js' // for default export or single inport
		import { Code1, Code2 } from 'module.js' //for mutiple import from the same file 
```




![[100  JavaScript Concepts you Need to Know(720P_HD).mp4]]