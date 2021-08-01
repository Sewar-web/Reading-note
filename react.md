# React 

- React : A JavaScript library for building user interfaces

**Hello World**

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);

```

**Introducing JSX**

* It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.


* Why JSX?
1. React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

2. Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.



```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);

```


```
function formatName(user) {
  return user.firstName + ' ' + user.lastName;
}

const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};

const element = (
  <h1>
    Hello, {formatName(user)}!
  </h1>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);

```

**Rendering Elements**

* Elements are the smallest building blocks of React apps.

`<div id="root"></div>` -> We call this a “root” DOM node because everything inside it will be managed by React DOM.

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```


* React Only Updates What’s Necessary
React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.



**Components and Props**

* Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to the idea of components

*
This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element.
`We call such components “function components” because they are literally JavaScript functions.`


*Rendering a Component*

* When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.


**Composing Components**

* Components can refer to other components in their output.

**Props are Read-Only**
Whether you declare a component as a function or a class, it must never modify its own props. Consider this sum function:

```function sum(a, b) {
  return a + b;
}
```


**State and Lifecycle**

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(
    element,
    document.getElementById('root')
  );
}

setInterval(tick, 1000);

```



**Converting a Function to a Class**

* You can convert a function component like Clock to a class in five steps:

1. Create an ES6 class, with the same name, that extends React.Component.
2. Add a single empty method to it called render().
3. Move the body of the function into the render() method.
4. Replace props with this.props in the render() body.
5. Delete the remaining empty function declaration.


**Adding Local State to a Class**

* We will move the date from props to state in three steps:

1. Replace this.props.date with this.state.date in the render() method:
2. Add a class constructor that assigns the initial this.state:
3. Remove the date prop from the <Clock /> element:

```
class Clock extends React.Component {
  constructor(props) {
    super(props);
    this.state = {date: new Date()};
  }

  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}

ReactDOM.render(
  <Clock />,
  document.getElementById('root')
);
```


**Adding Lifecycle Methods to a Class**

* In applications with many components, it’s very important to free up resources taken by the components when they are destroyed.

* We want to set up a timer whenever the Clock is rendered to the DOM for the first time. This is called “mounting” in React.

* We also want to clear that timer whenever the DOM produced by the Clock is removed. This is called “unmounting” in React.


**Handling Events**

* Handling events with React elements is very similar to handling events on DOM elements.

```
<button onclick="activateLasers()">
  Activate Lasers
</button>
```

Here, e is a synthetic event. React defines these synthetic events according to the W3C spec, so you don’t need to worry about cross-browser compatibility. React events do not work exactly the same as native events. See the SyntheticEvent reference guide to learn more.

When using React, you generally don’t need to call addEventListener to add listeners to a DOM element after it is created. Instead, just provide a listener when the element is initially rendered.

When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class. For example, this Toggle component renders a button that lets the user toggle between “ON” and “OFF” states:




**Passing Arguments to Event Handlers**
Inside a loop, it is common to want to pass an extra parameter to an event handler. For example, if id is the row ID, either of the following would work:

```
<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```


