
# Dynamic Rendering
Lets say we don't want to hard code all our values in our program, we can then dynamically render a value into a xml element and JSX will translate it accordingly

We can use
- computations (2+2)
- class variable this.state.....
- function

Using an component skeleton from [[React - Components]] and only showing the render function, 

<b>Hard coded</b>

	...
		render(){
			return (
				<div> 
					<h1>4</h1>
				</div>
			);
		}
	...

<b>Computation</b>

	...
		render(){
			return (
				<div> 
					<span>{2+2}</span>
				</div>
			);
		}
	...
	
<b>Class variable</b>

	...
		state = {
			count: 1 
		}
		render(){
			return (
				<div> 
					<span>{this.state.count}</span>
				</div>
			);
		}
	...
	
<b>Function</b>

	...
		render(){
			return (
				<div> 
					<span>{getCount()}</span>
				</div>
			);
		}

	getCount(){
		const count = 4 // Hard coded, could be class variable
		return count;
	}
	...

A function can also return a JSX expression

	getCount(){
		return <h1>Zero</h1>
	}
And it will be shown like a h1 






