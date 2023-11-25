
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


**useState()**
```
import {useState} from 'react';

export default function App() {
	// useState ONLY works if inside App function at top level
	const [isPressed, setPressed] = useState(false);

	function ToggleButton() {
		isPressed ? setPressed(false) : setPressed(true);
	}
  return (
	  <button onClick={ToggleButton}></button>
  )
}
```

**Three ways to conditionally output HTML**
1.  outer JSX
```
import {useState} from 'react';

function App() {
	const [showText, setShowText] = useState(false);

	function HandleText() {
		showText ? setShowText(false) : setShowText(true);
	}
	let welcomeText;
	
	if (showText) {
		welcomeText = <p>Hello! Welcome to my humble domain!</p>
	} else {
		welcomeText = null;
	}
	
	return (
		{welcomeText}
		<button onClick={HandleText}</button> 
	);
}

export default App;
```

2. inside JSX
```
import {useState} from 'react';

function App() {
	const [showText, setShowText] = useState(false);

	function HandleText() {
		showText ? setShowText(false) : setShowText(true);
	}
	
	return (
		{showText ? (<p>Hello! Welcome! Don't be shy...</p>) : null}
		<button onClick={HandleText}</button> 
	);
}

export default App;
```

3. &&
```
import {useState} from 'react';

function App() {
	const [showText, setShowText] = useState(false);

	function HandleText() {
		showText ? setShowText(false) : setShowText(true);
	}
	
	return (
		// If first statement is true -> output second statement
		{showText && <p>Hello there! Welcome in!</p>}
		<button onClick={HandleText}</button> 
	);
}

export default App;
```


**Dynamically output list of data**
```
const ArrayOfTodos [
]
export default function App() {
	
}
```