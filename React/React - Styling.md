# Styling
This is if you want to style your elements with to match your theme


## Using style attribute
We can style the elements ourselves with the style attribute, the style attribute takes in a plain JavaScript object

We can create one like this

	...
	styleObject={
		fontSize = 10,
		fontWeight = 'bold'
	}

	render(){
			return (
				<div>
					<span style={styleObject} >4</span>
				</div>
			);
		}
	...

This will set the text size to 10px, and set the font family to bold


## Using Bootstrap
If you have downloaded bootstrap we have some pre defined classes we can use for styling

	...
	render(){
			return (
				<div>
					<span className="badge badge-primary m-2">4</span>
				</div>
			);
		}
	...
Here we add the following classes to the span
- badge -> Gives a background to the text
- m-2 -> Gives a small margin to the text
- badge-primary -> Gives it a more primary look
For more see [[React - Extensions#Bootstrap]]


## Styling dynamically
In this example i am going to use bootstrap, we will add different class names depending on the value of the state variable count

We will go from this

	render(){
			return (
				<div>
					<span className="badge badge-primary m-2">4</span>
				</div>
			);
		}

to

	...
	render(){
		let classes = "badge m-2 badge-";
		classes += (this.state.count === 0) ? "warning" : "primary";
	
			return (
				<div>
					<span className={classes}>4</span>
				</div>
			);
		}
		...

We define the set classes in the classes variable and add "warning or "primary" depending on if count is 0 or not, However This can make the render function a little bloated. We can fix this by adding a function that returns the class names instead.

	...
	render(){
			return (
				<div>
					<span className={this.getBadgeClasses()}>4</span>
				</div>
			);
		}

		getBadgeClasses(){
			let classes = "badge m-2 badge-";
			classes += (this.state.count === 0) ? "warning" : "primary";
			return classes;
		}
		...