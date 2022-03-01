# Boolean operands with non boolean expressions
In JSX you can use non boolean expressions in order to get a simple do if operation
Normal code


	Statement: true && true
	Result: true

-----------------------
	
	Statement: true && false
	Result: false

----------------------
	
	Statement: false && false
	Result: false
	
---
These work like normal, however lets see what happens when we get non boolean expressions in a statement


	
	Statement: true && "Hello"
	Result: "Hello"

---
	
	Statement: false && "Hello"
	Result: false

---
Now we get the string back as a result if the condition is true, we can manipulate this to show different elements if a condition is true
Example

	render(){
		return(
			<div>
				<p>{this.state.value === 0 && "The value is zero"}</p>
			</div>	
		);
	}

We can also do this with whole elements

	{this.state.value === 0 && <p>"The value is zero"</p>}