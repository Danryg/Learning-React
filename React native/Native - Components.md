# Components

## Props or attributes
Certain components has it's own attributes or props that can be set to satisfy the interface

## View
	<View></View>

This is the most fundamental component, it works like a div. You use this to group children or have certain styles associated to all elements within it

### Safe are view
<SafeAreaView></SafeAreaView>

SafeAreaView is in it self the same component, however it only covers the parts of the phone that could not be covered in any way by the "notch" on iPhone or the battery and system information on top of the screen interface.


## Text
	<Text>This is my text</Text>

This component is used to display text, the text component has many interesting props
Example

<b>number of lines</b>
The text will be truncated if longer than one line

		<Text numberoflines = {1}>If this text is longer than one line it will be 
		truncated </Text>


## Images

	<image></image>

Set an image

Local

	<image source={require('./filepath')} />

Require returns a number that is the reference to our image

Internet

	<image source={{ uri: 'https://webpagething.photos/200/300'}} />


## Touchables
Some component does not have the onPress event that allows the user to press on that component for something to happen

### Touchablewithoutfeedback
This component does not implement any visible feedback when pressed

	<TouchableWithoutFeedback></TouchableWithoutFeedback>

We can put components inside this component, we can then add an onPress event on this component for it to call a function or do something else when pressed

	<TouchableWithoutFeedback onPress= {()=>console.log("Touched")}></TouchableWithoutFeedback>


### TouchableOpacity
This component fives a visual feedback when pressed, the components inside will be set to 0 opacity and quickly turn back to normal opacity

	<TouchableOpacity></TouchableOpacity>

### TouchableHighlight
This component will quickly highlight the component when it is pressed


	<TouchableHighlight> </TouchableHighlight>

### TouchableNativeFeedback
This will quickly make an expanding circle from where the component was pressed
> OBS! this only works on android

	<TouchableNativeFeedback></TouchableNativeFeedback>


## Buttons
Buttons are very different from IOS to Andoroid o be carefull using this component

	<Button> </Button>

## Alert
Alerts are used to display a small box with a message, this works a bit different these are opened with a function.

<b>alert()</b>
This will give a normal alert with a title, message and buttons
Example

	<Button onPress={() => 
				Alert.alert("title", "message", [
					{text: "thing" onPress: ()=> console.log("thing pressed")}
					{text: "thing2" onPress: ()=> console.log("thing2 pressed")}
				])
			}
		/>

<b>prompt()</b>
> <text style = "color:red">OBS Prompt only works on IOS</text>

This will prompt the user to write a message
Example

	<Button onPress={() => 
			Alert.prompt("title", "message", (text)=> console.log("user wrote", text))
		}
	/>





