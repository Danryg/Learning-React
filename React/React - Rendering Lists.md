# Rendering Lists
Let's imagine you want to render a list of elements in a component, JSX translates the code in such a way that you can not use loops like in normal JS but instead we use another syntax. We have a list of tags in the state variables

	...
	state ={
		tags: ['tag1', 'tag2', 'tag3']
	}
	...

and we want to render these as different list items in an unordered list. We can then use the syntax, we also need to give each li an unique key

	...
	<ul>
		{this.state.tags.map(tag => <li key = "uniqueID">{tag}</li>)}
	</ul>
	...


## Conditional Rendering
In JSX there are no if or else statements, so we need to go back into plain old JS
We can accomplish this using a helper function. Since all the tags are unique we can use them as id for the lis

	...
	state ={
		tags: ['tag1', 'tag2', 'tag3']
	}
	
	renderTags(){
		if(this.state.tags.length === 0) return <p>There are no tags</p>;

		return <ul>{this.state.tags.map(tag => <li key = {tag}>{tag}</li>)</ul>
	}

	render(){
		return(
			<div>
				{this.renderTags()}	
			</div>
		);
	}
