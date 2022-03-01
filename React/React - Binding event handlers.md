# Binding event handlers
When you have created a standalone function in lets say a component it does not have access to the object it is called from the " this " object. We can fix this by binding the function to the object in the constructor
We accomplish this by doing the following in the constructor

		constructor(){
			super();
			this.myEventHandler.bind(this);
		}
Notice that in this example the class extends component and needs to call super(); before anything else.

Component Example


	class myCom extends Component{
		state ={
			value: 0;
		}

		constructor(){
			super();
			this.myEventHandler.bind(this);
		}

		myEventHandler(){
			console.log("The object: ", this)
		}

		render(){
			return(
				<button onClick={this.myEventHandler()} >Press me</button>
			);
		}
	}

## Arrow functions
Arrow functions in JS inherits the this object by default
so in the following example you do not need to bind the handler

	myEventHandler= () =>{
		console.log(" The object that handle this event is ", this)
	}

