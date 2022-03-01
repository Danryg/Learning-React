# Composing components
When we have a lot of components , some use other components. We can draw a component tree out of this
Example:
![[compTree.png]] 
But in order for a component to use another we will need to create components inside another component.  Lets see how we do that

<b>Basic example </b>
Using the [[Counter - basic]]I am going to create a counters class that includes a div with 4 counter objects

	

	import React, {component} from 'react';
	import Counter from './counter'

	class Counters extends Component{
		state ={}
		render(){
			return(
				<div>
					<Component />
					<Component />
					<Component />
					<Component />
				</div>
			);
		}
	}


