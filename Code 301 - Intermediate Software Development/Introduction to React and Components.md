
# react JS:
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

 #### Extracting Components:
we can divied componantes into smaller one.


[](data:image/jpeg;base64,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)
