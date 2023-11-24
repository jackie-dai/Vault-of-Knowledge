
Props


**alternate syntax**
```
function MenuItem({image, name, description}) {
	<div>
		<img src={image}/>
		<p>{name}</p>
		<p>{description}</p>
	</div> 
}

```

function App() {
	return (
	
		<MenuItem  {...MENU_ITEMS[0]}/>
		
		<MenuItem  {
			MENU_ITEMS[1].image
			MENU_ITEMS[1].name
			MENU_ITEMS[2].description
			)}/>
	)
}



Special Props Property\: Children **

```
export function TabButton({props}) {
	return (
			<ul>
				<li><button>props.children</button></li>
			</ul>
	);
}

function App() {
	return (
		<TabButton>Whatever goes in here will be inside children</TabButton>
	)
}

export default App;

```


Dynamic Arguments 
```
function printHelloWorld() {
	console.log("Hello World");
}

function printName(name) {
	console.log("Hello " + name);
}

export function CustomButton(onClick, func) {
	return (
		<div><button onClick={func}></button></div>
	)
}

function App() {
	return (
		<CustomButton onClick=""></CustomButton>
	)
}

export default App;
```