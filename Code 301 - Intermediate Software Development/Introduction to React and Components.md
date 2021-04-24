
# React JS:
React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called “components”.

A component takes in parameters, called props (short for “properties”), and returns a hierarchy of views to display via the render method.
- Square
- Game
in the toturiol it showed us how to build a tiktak game.

## JSX
const element = <h1>Hello, world!</h1>; we called this jsx recommend using it with React,Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.

### starting Code 

```class Square extends React.Component {
  render() {
    return (
      <button className="square">
        {/* TODO */}
      </button>
    );
  }
}

class Board extends React.Component {
  renderSquare(i) {
    return <Square />;
  }

  render() {
    const status = 'Next player: X';

    return (
      <div>
        <div className="status">{status}</div>
        <div className="board-row">
          {this.renderSquare(0)}
          {this.renderSquare(1)}
          {this.renderSquare(2)}
        </div>
        <div className="board-row">
          {this.renderSquare(3)}
          {this.renderSquare(4)}
          {this.renderSquare(5)}
        </div>
        <div className="board-row">
          {this.renderSquare(6)}
          {this.renderSquare(7)}
          {this.renderSquare(8)}
        </div>
      </div>
    );
  }
}

class Game extends React.Component {
  render() {
    return (
      <div className="game">
        <div className="game-board">
          <Board />
        </div>
        <div className="game-info">
          <div>{/* status */}</div>
          <ol>{/* TODO */}</ol>
        </div>
      </div>
    );
  }
}

// ========================================

ReactDOM.render(
  <Game />,
  document.getElementById('root')
);



```

#### Embedding Expressions in JSX:
an put any valid JavaScript expression inside the curly braces in JSX

after compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

#### Specifying Attributes with JSX
we can use quotes.
use curly braces.
Specifying Children with JSX: close it immediately with />

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

in your file “root” DOM node because everything inside it will be managed by React DOM.
React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

Even though we create an element describing the whole UI tree on every tick, only the text node whose contents have changed gets updated by React DOM.

#### Components and Props:
Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.

#### Function and Class Components:
This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

 ### Rendering a Component:
When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.

#### Composing Components:
Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

 


![](https://www.webrexstudio.com/wp-content/uploads/2019/05/react-js-image.png)
