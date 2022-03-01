# Updating a state variable
In a component you can not just set a value to a state variable outside of the state brackets, instead you use the this.setState() function


	state = {
		value: 0
	}
	myFunction = () =>{
		this.setState({value: 2});
	}

This will set value of the value variable from 0 to 2

<b>Increment</b>
	
	myFunction = () =>{
		this.setState({value: value + 1});
	}

<b>Decrement</b>

	myFunction = () =>{
		this.setState({value: value - 1});
	}

### What happens?
this.setState(....) function does multiple things to make sure that the state variables value is changed and that the change is rendered to the screen
The setState function does the following
- Calls the render function in the component
	- returns a new react element 
		- creates a new virtual DOM
- React compares the new virtual DOM to the old virtual DOM and switches the elements that have changed