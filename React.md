
Props



***
**alternate syntax**
function MenuItem({image, name, description}) {
	<div>
		<img src={image}/>
		<p>{name}</p>
		<p>{description}</p>
	</div> 
}
***

function App() {
	return (
		<MenuItem />
	)
}