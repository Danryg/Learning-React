# Passing data into components
We are going to make some modifications to the [[Counter - basic]] so that we can pass in data when we create a component

We start by adding counters from a list instead of hard coding them

	import React, {component} from 'react';
	import Counter from './counter'

	class Counters extends Component{
		state ={
			counters: [
				{id: 1, value: 4},
				{id: 2, value: 0},
				{id: 3, value: 0},
				{id: 4, value: 0}
			]
		}
		render(){
			return(
				<div>
					{this.state.counters.map(counter => 
						<Counter key={counter.id} value={counter.value} selected={true}/>)}
				</div>
			);
		}
	}

You can now see that we pass in an attribute called value into the counter, this will go into the props property in the counter. Every component has a props property that can be used to pass in data

	import React, { Component } from React

	class Counter extends Component{
		state = {
			value = this.props.value;
		}

		render(){
			return(
				<div>
					<span>{this.formatCount()}</span>
					<button onClick={this.handleIncrement}>Increment</button>
				</div>		
			);
		}

		formatCount(){
			const {count} = this.state;
			return === 0 ? 'Zero' : count
		}
		
		handleIncrement = () =>{
			this.setState({value: this.state.value + 1});
		}
	}

You can now see that we use the this.props.value to set the state variable value in the component


