State and Lifecycle:
 (Links to an external site.)React.Component:
 (Links to an external site.)React lets you define components as classes or functions. Components defined as classes currently provide more features which are described in detail on this page. To define a React component class, you need to extend React.Component:
image

 (Links to an external site.)The only method you must define in a React.Component subclass is called render(). All the other methods described on this page are optional.
 (Links to an external site.)The Component Lifecycle:
 (Links to an external site.)Each component has several “lifecycle methods” that you can override to run code at particular times in the process. You can use this lifecycle diagram as a cheat sheet. In the list below, commonly used lifecycle methods are marked as bold. The rest of them exist for relatively rare use cases.
image

 (Links to an external site.)Mounting
 (Links to an external site.)These methods are called in the following order when an instance of a component is being created and inserted into the DOM:
1-constructor()

2-static getDerivedStateFromProps()

3-render()

4-componentDidMount()

 (Links to an external site.)Updating
 (Links to an external site.)An update can be caused by changes to props or state. These methods are called in the following order when a component is being re-rendered:
1-static getDerivedStateFromProps()

2-shouldComponentUpdate()

3-render()

4-getSnapshotBeforeUpdate()

5-componentDidUpdate()

 (Links to an external site.)Unmounting
 (Links to an external site.)This method is called when a component is being removed from the DOM:
componentWillUnmount()

 (Links to an external site.)Handling Events:
 (Links to an external site.)Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:
1-React events are named using camelCase, rather than lowercase.

2-With JSX you pass a function as the event handler, rather than a string.

 (Links to an external site.)for example, the HTML:
image

 (Links to an external site.)is slightly different in React:
image

 (Links to an external site.)Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly. For example, with plain HTML, to prevent the default link behavior of opening a new page, you can write:
image

 (Links to an external site.)In React, this could instead be:
image

 (Links to an external site.)When using React, you generally don’t need to call addEventListener to add listeners to a DOM element after it is created. Instead, just provide a listener when the element is initially rendered.
 (Links to an external site.)When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class. For example, this Toggle component renders a button that lets the user toggle between “ON” and “OFF” states:
image

 (Links to an external site.)Conditional Rendering:
 (Links to an external site.)In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.
 (Links to an external site.)Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.
 (Links to an external site.)Consider these two components:
image

 (Links to an external site.)We’ll create a Greeting component that displays either of these components depending on whether a user is logged in:
image
