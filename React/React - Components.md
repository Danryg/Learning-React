# Components

## JSX component skeleton
This is a JSX component skeleton to get started

	import React, { Component } from 'react';

	class componentName extends Component {
		state = {}
		render() {
			return (...)
		}
		
	}
	export default componentName;

You can create this quickly with the extension [[React - Extensions#Simple react snippet]]. Use the quick command 

	imrc - imports react component
and use 

	cc - creates the class code

## How it looks
What the component looks like is determined by what is returned in the render function in the class
	
	render() {
		return <h1>Hello World</h1>
	}
	

In order to return  multiple objects you need to wrap it in a bigger component

	render() {
		return (
			<div>
				<h1>Hello World</h1>
				<button>Increment</button>
			</div>
		);
	}


## How to use components

In the Index.js file write

	ReactDOM.render(<ComponentName />, container);


## Example code

<b>Counter.jsx</b>

	import React, { Component } from 'react';

	class Counter extends Component {
		state = {}
		render() {
			return <h1>Hello World</h1>;
		}
		
	}
	export default Counter;

<b>Index.js</b>

	import Counter from '.components/counter'
	
	ReactDOM.render(<Counter />, document.getElementById('root'))
	

