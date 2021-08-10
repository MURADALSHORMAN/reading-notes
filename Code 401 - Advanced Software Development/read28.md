### Why do we not need more .html pages in a multi-page React app?
In the Multipage apps , we split up our components but a lot of pages are going to be normal HTML pages, and widgets we dump in like an Image gallery that is managed by React, so the entire page is not under React control.
### If we wanted a component to show up on every page, where would we put it and why?
Inside a < Route />: because React Router is a standard library for routing in React. It enables the navigation among views of various components in a React Application, allows changing the browser URL, and keeps the UI in sync with the URL.
### What does routing do with the components that were rendered when a new route is requested?
One way to do would be to pass the component prop an inline function. When you use component, the router uses React. createElement to create a new React element from the given component. That means if you provide an inline function to the component prop, you would create a new component every render.
### What does props.children contain?
props.children represents the content between the opening and the closing tags when invoking/rendering a component.
can have one element, multiple elements, or none at all, its value is respectively a single child node, an array of child nodes or undefined.

### How do useState() and this.setState() differ
setState is merging the previous state with the new one, it means that you dont have to pass the full state object every time you want to change some part of the state. React will update given properties and won’t touch the rest. The useState’s updater rewrites a previous state with a new one and it does not perform any merging. Its just replacement instead of merging.

### Document the following Vocabulary Terms: (Links to an external site.)
	 
- State Hook	the State of a component is an object that holds some information that may change over the lifetime of the component.and Hook that allows you to have state variables in functional components , it takes the initial state as an argument and returns an array of two entries.

- Mounting and Un-Mounting	Mounting is the process of outputting the virtual representation of a component into the final UI representation (e.g. DOM or Native Components). & Un-Mounting: This method is called just before the component gets destroyed. Any clean up statements should be executed inside this method.


## Using the Effect Hook
#### What does useEffect do? 
- By using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed (we’ll refer to it as our “effect”), and call it later after performing the DOM updates. In this effect, we set the document title, but we could also perform data fetching or call some other imperative API.

#### Why is useEffect called inside a component? 
- Placing useEffect inside the component lets us access the count state variable (or any props) right from the effect. We don’t need a special API to read it — it’s already in the function scope. Hooks embrace JavaScript closures and avoid introducing React-specific APIs where JavaScript already provides a solution.


