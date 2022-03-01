# Embedded Expressions
Lets say we don't want to hard code all our data in our program, we can then use state variables, functions with a combination of computations to have our data update dynamically

We use the mark-up element span to do this, check the JSX note [[JSX - Dynamic Rendering]] to see how we can use different ways of dynamically format in JSX

Example

	class Counter extends Component{
		state = {
			count: 1
		};

		render(){
			return (
				<div>
					<span>{this.formatCount()}</span>
				</div>
			);
		}

		formatCount(){
			const {count} = this.state;
			return === 0 ? 'Zero' : count
		}
	}

This code, if the count state variable is 0 then shows 'zero' as text instead of a number.


	

