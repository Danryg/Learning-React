# Component life-cycle

There are some inherited methods in a component that are automatically called during the life cycle of a component. There are three different phases.

- Mount
- Update
- Unmount

The methods that can be created to be called during one of these phases are called life-cycle hooks.

## Mount
The mount face starts when the component is created/instantiated

## Update
This happens when the state or props of the component undergoes a change

## Unmount
This happens right before the component is deleted from the DOM


## Life-cycle hooks
<b>Mount</b>
- constructor 
- render 
- componentDidMount 

<b>Update</b>
- render
- componentDidUpdate

<b>Unmount</b>
- componentDidUnmount

There are more life cycle hooks that are rarely used