# Stateless Functional Component
This is a component that has no state and is purely functional, instead of using a class to define the component we can use a function


<b>Class definition</b>

	import React, { Component } from 'react'
	
	class myComponent extends Component{
		render(){	
			return(
				.....
				..elements
				......
			);
		}
	}

	export default myComponent


<b>Function definition</b>

	import React, { Component } from ' react';

	const NavBar = (props ) =>{
		return(
			.....
			..elements
			......
		);
	}

	export default Navbar

Note that you need to pass the props object as a parameter if it is used by the elements
