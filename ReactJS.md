## ReactJS

### What is react js?

A javascript library for building user interface

### What is JSX?

A syntax extension for javascript that allows HTML-Like code

### What is component in react?

A reusable piece of code that represents a UI element

### What is difference between state and props

State changes are within a component, while props are immutable of data

### How do handle event in react?

Using event handlers like onClick, onChange

### What is the virtual DOM?

A lightweight in memory DOM implementation representation of the real DOM

### How does react handle rendering

Using a reconciliation algorithm to determine DOM changes

### What is HOC?

A function that takes a component and return a new component

### What is react hook?

A way to use state and other react features in function components

### What is difference between react and angular ?

React is a library while angular is a full-featured framework

### How do you optimize react performance?

Using memoization, shouldComponentUpdate, and code splitting

### What is the react context

A way to share data between components without passing props

### How do you handle errors in react?

Using try-catch blocks, error boundaries, and componentDisCatch

### What is the react fragment?

A way to group elements without adding an extra DOM structure node

### How do you use react with typescript?

Using @types/react and @types/react-dom packages

### What is a controlled component?

A component that stores in state the parent component

### What is uncontrolled component?

A component that store in state internally

### What is difference between createElement and cloneElement?

Create element create new element, while cloneElement clones an existing element

### How do you implement server side rendering in React?

Using nextjs or similar framework

### What is react portal?

A way to render a component outside the parent component's DOM

### How do you use react ref?

To access DOM elements for child components

### What is difference between useState and useReducer?

useState is for simple state updates, while useReducer for complex state logic

### How do you handle side effects in react?

Using useEffect or useLayoutEffect hooks

### What is a React Lazy?

A way to lazy load a component components or modules

### How do you use React router?

To handle client side routing and navigation

### What is the features of React?

1. Jsx: JSX servers as a syntax extension to JS, facilitating the combination of HTML structures with JS code within React Files.

2. Component: JSX servers as a syntax extension to JS, facilitating the combination of HTML structures with JS code within React Files.

3. Virtual DOM: React employs a virtual DOM, which is a lightweight representation of the actual DOM stored in memory. This approach allows React to selectively update only the relevant parts of the real DOM when state of an object changes.

4. Data binding: React adopted a one way data binding approach, ensuring a modular and efficient structure. Unidirectional data flow signifies that in a React app, child components are often nested within parent components

5. High performance: React's high performance is driven by its ability to update only the components that undergo changes, rather than refresh the entire. This results in significant faster web application.

### What is different between element and component in React?

1. Element: is a simple object that describe what you want to show on the screen. It defines the structure of a DOM nodes or other components. Element can include other elements in their props. Once created, elements cannot be changed. Creating react element is a straightforward and inexpensive operation.

```bash
## with jsx
const element = <div id="btn-login">Login</div>

## without jsx
const element = React.createElement("div", { id: "btn-login", "Login" });
```

2. Component: can be declared in various ways. It can be a class with a render() method, or it can be defined as a function. Components take props as a input and return a JSX tree as output. Components are more powerful and flexible compared to Elements

```bash
## using JSX
const Button = ({ handleFunc }) => {
  return (
    <div id="btn-login" onClick={handleFunc}>
      Login
    </div>
  )
}

## transpiled
const Button = ({ handleFunc }) => {
  React.createElement(
    "div,
    {
      id: "btn-login",
      onClick: handleFunc,
    },
    "Login",
  )
}
```

[More Info](https://www.linkedin.com/in/vaibhav0524/recent-activity/all/)
