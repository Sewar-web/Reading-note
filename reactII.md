# React 


* In React, you can create distinct components that encapsulate behavior you need. Then, you can render **only** some of them, depending on the state of your application.


* Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.


* If you want render a part of the component while the rest of the output doesn’t change,you can use variables to store elements.

* When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort

* Keys only make sense in the context of the surrounding array.

* Keys used within arrays should be unique among their siblings. However they don’t need to be globally unique. We can use the same keys when we produce two different arrays
HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state.

* n most cases, it’s convenient to have a JavaScript function that handles the submission of the form and has access to the data that the user entered into the form. The standard way to achieve this is with a technique called “controlled components”.
In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().


* You may embed expressions in JSX by wrapping them in curly braces. This includes the JavaScript logical && operator. 


* In rare cases you might want a component to hide itself even though it was rendered by another component. To do this return null instead of its render output.


* You can build collections of elements and include them in JSX using curly braces {}.

* **Keys** help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys.


* In HTML, form elements such as < input >, < textarea >, and < select > typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.


* **what happens when you edit an input?** :
  
1.  React calls the function specified as onChange on the DOM < input >. In our case, this is the handleChange method in the TemperatureInput component.
  
2. The handleChange method in the TemperatureInput component calls this.props.onTemperatureChange() with the new desired value. Its props, including onTemperatureChange, were provided by its parent component, the Calculator.
  
3. When it previously rendered, the Calculator had specified that onTemperatureChange of the Celsius TemperatureInput is the Calculator’s handleCelsiusChange method, and onTemperatureChange of the Fahrenheit TemperatureInput is the Calculator’s handleFahrenheitChange method. So either of these two Calculator methods gets called depending on which input we edited.
  
4. Inside these methods, the Calculator component asks React to re-render itself by calling this.setState() with the new input value and the current scale of the input we just edited.
  
5. React calls the Calculator component’s render method to learn what the UI should look like. The values of both inputs are recomputed based on the current temperature and the active scale. The temperature conversion is performed here.
  
6. React calls the render methods of the individual TemperatureInput components with their new props specified by the Calculator. It learns what their UI should look like.
  
7. React calls the render method of the BoilingVerdict component, passing the temperature in Celsius as its props.
  
8. React DOM updates the DOM with the boiling verdict and to match the desired input values. The input we just edited receives its current value, and the other input is updated to the temperature after conversion.


* React has a powerful composition model, and we recommend using composition instead of inheritance to reuse code between components.


* JSX — Allows us to write HTML like syntax which gets
transformed to lightweightJavaScript objects.


* Virtual DOM — A JavaScript representation of the actual
DOM.


* React.Component — The way in which you create a new component.

* render (method) — Describes what the UI will look like for
the particular component.

* ReactDOM.render — Renders a React component to a DOM node.

* state — The internal data store (object) of a component.

* constructor (this.state) - The way in which you establish
the initial state of a component.

* setState — A helper method used for updating the state of a
component and re-rendering the UI

* props — The data which is passed to the child component
from the parent component.

* propTypes — Allows you to control the presence, or types of
certain props passed to the child component.

* defaultProps — Allows you to set default props for your component.

* **Component LifeCycle**
  - componentDidMount — Fired after the component mounted
  
  - componentWillUnmount — Fired before the component will unmount
  
  - getDerivedStateFromProps - Fired when the component mounts and

* whenever the props change. Used to update the state of a
component when its props change

**Events**
  - onClick
  
  - onSubmit
  
  - onChange
