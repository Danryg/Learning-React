# Events
All elements have properties that handle standard DOM events
- onClick
- onDoubleClick
- onKeyDown
- ....
We can then embedd a function into that attribute
Example:

	handleButtonPress(){
		console.log("The button is pressed");
	}


	render(){
		return(
			<div>
				<button onClick={this.handleButtonPress}>Press me</button>
			</div>
		);
	}

## Passing event arguments
In react we can not just put parentheses and put arguments within the onClick attribute, instead we have two ways of doing it.

These are 2 examples showing how to pass in an JSX object with an attribute of id with value 1 as an input argument to the function

<b>Another Function</b>

	handleButtonPress(product){
		console.log("The button is pressed");
	}

	onHandleButtonPress = () =>{
		this.handlebuttonPress({id: 1});
	}

	render(){
		return(
			<div>
				<button onClick={this.onHandleButtonPress}>Press me</button>
			</div>
		);
	}

<b> Arrow function as value in the attribute</b>

	handleButtonPress(product){
		console.log("The button is pressed");
	}



	render(){
		return(
			<div>
				<button 
				onClick={() => this.handlebuttonPress({id: 1})}>Press me</button>
			</div>
		);
	}

