# Debugging



## Logging
This will send out a message to the terminal

	Console.log(" Message ");

Remember that if you have 2 virtual devices running, it will send out one log message for each device. This also negatively affects performance so only use it in development and production.


## Chrome
Open up the developer menu and enable remote debugging, this will open up chrome. Now open up chrome developer tools and look at the console tab and you can see any logs and messages. If you want debug the code line by line go to the Sources tab and press pause on caught exceptions. When we reload the app and there is an exception the chrome developer tools will pause the program and  you can see exactly where the exception was thrown.

<mark style="color: red"> OBS! Enabling remote debug makes the app slow, turn off when done</mark>

<b>Breakpoint</b>
Press on any line number to set a breakpoint

<b>Watch</b>
On the right there is a watch component where you can type in the name of a variable. That variable will then be watched. 

## Visual Studio Debugg

<mark style="color: red">Make sure you got React native tools extension installed in VS code</mark>

Go to the debug menu in VS code and create a launch.json file, pick react native in the drop down menu, select  attach to packager and click ok

Go into the launch.json file, click the run tab in the top menu and click 
"*create configuration*", start typing "*reactnative:*" now you will se a set of different pre made configs that you can choose from

Save the changes and Enable remote debugg in your emulator or phone. Then go into 
Code>Preferences>Settings search for "*react-native.packager.port*" change the port to the same as the remote debugger. 

<mark style="color: red">OBS! Close the react native debugger before running</mark>

Run the debugger in the  debugger menu in VS code, then go into
view>debug console

Reload the app and it will stop at any exceptions or breakpoints it encounters and you can step over the code line by line

<mark style="color: red"> OBS! Enabling remote debug makes the app slow, turn off when done</mark>


