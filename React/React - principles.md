# Principles
These are principle that should be followed when coding in react

--- 
## Single source of truth
An violation of this is when you set a state variable in a component that is set from an outside source and that changes throughout as the program is used. If we then were to change the value outside of the component, the value in the state of the component remains unchanged. There are multiple sources of truth

To combat this we use events so that the component of which determines the value now is responsible for changing it.

## Parents should be the ones modifying the children
This is commonly violated when you let a child remove itself from the component, this means that the child changes the state of the parent 