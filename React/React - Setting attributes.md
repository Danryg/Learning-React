# Setting attributes
Lets say, while creating a component we want to set some attributes for the elements.

Don't know what a component is? Read [[React - Components]]

### Using JSX
In the img element we need to set the src attributes so it knows what picture to show, we can do this by writing src="" between the tags
	class Counter extends Component{

		render(){
			return (
				<div>
					<img src="https://picsum.photos/200"></img>
				</div>
			);
		}
	}


### Using Embedded expressions
Read [[React - Embedded Expressions]]

	class Counter extends Component{
		state = {
			imageUrl: "https://picsum.photos/200" 
		};

		render(){
			return (
				<div>
					<img src={this.state.imageUrl}></img>
				</div>
			);
		}
	}


