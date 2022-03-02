# Destructuring
If you notice that your code has a lot of this.props in it you can simplify the code by importing specific functions, objects or variables directly from the component using destructuring


instead of using

	this.props.value
	this.props.onEvent1
	this.props.onEvent2
	this.props.onDelete

We can write

	const {value, onEvent1, onEvent2, onDelete} = this.props;

	value
	onEvent1
	onEvent2
	onDelete

