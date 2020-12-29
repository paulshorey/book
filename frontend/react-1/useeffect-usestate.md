# hooks \(useEffect, etc\)

**`useRef`** 

**`useCallback`** 

**`useState` uses a tuple** to define   
**first** the variable name,   
**then** the name of the function which should be called to set the variable to a new value. This is the alternative to `setState` which could update any/all state variables. This one is specific to the one variable which is the first item in the tuple.   
**Finally after the equal sign** is the  `useState()` function. Pass to this function a value, the initial value which your variable should have.

**`useEffect` is a combination** of `componentDidMount` and `componentDidUpdate` and some other lifecycles. Put code into here which will call useState handlers after data is gotten, or some event happens.

**Replace componentDidUpdate and other methods with useEffect:** [https://www.digitalocean.com/community/tutorials/react-replacing-component-lifecycles-with-useeffect](https://www.digitalocean.com/community/tutorials/react-replacing-component-lifecycles-with-useeffect)

