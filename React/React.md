
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

export function CustomButton({onClick}) {
	return (
		<div><button onClick={onClick}></button></div>
	)
}

function App() {
	return (
		// Always pass in function name. DO NOT EXECUTE. Let react execute.
		<CustomButton onClick={printHelloWorld}></CustomButton>

		// Use arrow function when passing in arguments
		<CustomButton onClick={() => printName("Jackie")}></CustomButton>
	)
}

export default App;
```