	import React, { Component } from React

	class Counter extends Component{
		state = {
			value = 0;
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
			this.setState({value: value + 1});
		}
	}
	