# Components

## Props or atributes
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

