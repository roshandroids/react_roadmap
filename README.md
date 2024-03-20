# React Developer Roadmap (WIP)

## Welcome!

Welcome to the React Developer Roadmap! This interactive guide is designed to help aspiring and experienced React developers navigate their learning journey and excel in the React ecosystem.

## Important Note:

🚧 **Work in Progress**: This roadmap is continually evolving, with new content added and existing sections refined regularly. Stay tuned for updates!

## How to Use This Roadmap:

This roadmap is highly adaptable to your learning style and career goals. Feel free to explore topics in any order that suits you best.

- **Beginner?** Start from the basics and gradually progress to advanced concepts.
- **Experienced?** Dive into specific topics or areas where you want to enhance your skills.
- **Have Feedback or Suggestions?** We value your input! Share your thoughts, report errors, or suggest improvements via:
  - Creating a new issue on the [GitHub repository](https://github.com/roshandroids/react_roadmap/issues).
  - Submitting a pull request (PR) with your proposed changes.

Let's embark on this exciting journey together and build amazing things with React!

The topics are taken and article is generated based on roadmap listed on [https://roadmap.sh/react](https://roadmap.sh/react).

---

# React Roadmap

## Table of Contents

- [Vite](#vite)
- [Components](#components)
  - [Functional Components](#Functional-Components)
  - [JSX](#jsx)
  - [Props](#props)
  - [State](#state)
  - [Conditional Rendering](#conditional-rendering)
- [Rendering](#rendering)
  - [Component Lifecycle](#component-lifecycle)
  - [Lists and Props](#lists-and-props)
  - [Render Props](#render-props)
  - [Events](#events)
  - [Higher Order Components and Functions](#higher-order-components-and-functions)
- [Hooks](#hooks)
  - [useState](#usestate)
  - [useEffect](#useeffect)
  - [useContext](#usecontext)
  - [useReducer](#usereducer)
  - [useCallback](#usecallback)
  - [useRef](#useref)
  - [useMemo](#usememo)
  - [Custom Hooks](#custom-hooks)
- [Routing](#routing)
  - [React Router](#react-router)
- [State Management](#state-management)
  - [Zustand](#zustand)
- [Styling](#styling)
  - [Tailwind](#tailwind)
  - [Bootstrap](#bootstrap)
- [API Calls](#api-calls)
  - [GraphQL](#graphql)
  - [REST](#rest)
- [Testing](#testing)
  - [Jest](#jest)
  - [React Testing Library](#react-testing-library)
- [Frameworks](#frameworks)
  - [Next.JS](#nextjs)
  - [Vue.JS](#vuejs)
- [Forms](#forms)
  - [React Hook Form](#react-hook-form)
- [Advanced Topics](#advanced-topics)
  - [Suspense](#suspense)
  - [Portals](#portals)
  - [Error Boundaries](#error-boundaries)
  - [Fiber Architecture](#fiber-architecture)
- [Mobile](#mobile)
  - [React Native](#react-native)

---

# Vite:

Vite is a modern build tool specifically designed to **enhance the development experience** for front-end web applications. Here is the breakdown of information regarding vite.

> **Focus:** Lightning-fast development experience with instant hot module replacement (HMR).
>
> **Why Use It:**
>
> - **Blazing Speed:** Near-instantaneous server startup and hot module replacement for rapid development cycles.
> - **Simplicity:** Easy to set up and use, reducing configuration overhead.
> - **Modern Features:** Supports latest web technologies like TypeScript, JSX, and CSS preprocessors.
>
> **When to Use:**
>
> - Projects that prioritize development speed and a smooth workflow.
> - Modern web development using popular frameworks (React, Vue.js, Svelte).
>
> **Official Documentation:**
>
> [Vite](https://vitejs.dev/)
>
> Vite offers a streamlined approach to front-end development, ideal for projects where development speed and a pleasant experience are paramount.

---

# Components

- **Functional Components**
  > **Focus:** Simple, stateless UI building blocks that return JSX.
  >
  > **Why Use Them:**
  >
  > - **Concise Syntax:** Easier to write and understand compared to class components.
  > - **Presentational Components:** Ideal for displaying data and don't require complex state management.
  > - **Reusable:** Can be easily reused throughout the application.
  >
  >   **When to Use:**
  >
  > - Building simple UI components that focus on rendering.
  > - Prefer a more streamlined development approach.
  >   **Example:**
  >
  > ```jsx
  > function Greeting(props) {
  >   return (
  >     <div>
  >       <h1>Hello, {props.name}!</h1>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Further Resources:**
  >
  > - React Documentation: [https://react.dev/learn/javascript-in-jsx-with-curly-braces](https://react.dev/learn/javascript-in-jsx-with-curly-braces)
- **JSX**
  > **Focus:** Syntax extension for embedding HTML-like structures within JavaScript.
  > **Why Use It:**
  >
  > - **Intuitive UI Definition:** Resembles HTML, making it easier to visualize and write UI elements.
  > - **Dynamic Content:** Allows embedding JavaScript expressions for dynamic rendering.
  >   **When to Use:**
  >
  > - Defining the UI structure of React components.
  > - Mixing HTML-like elements with JavaScript logic for interactive components.
  >   **Example:**
  >
  > ```jsx
  > function Greeting(props) {
  >   return (
  >     <div>
  >       <h1>Hello, {props.name}!</h1>
  >     </div>
  >   );
  > }
  > ```
- **Props**
  > **Overview:**
  >
  > - **Focus:** External data passed down from parent to child components.
  > - **Read-only:** Cannot be modified within the receiving component.
  >   **Why use Props:**
  >
  > - **Data Sharing:** Enables components to receive data from their parents.
  > - **Component Reusability:** Promotes reusable components that can accept different props.
  >   **When to use Props:**
  >
  > - Passing data from a parent component to its children.
  > - Defining configuration options for child components.
  >   **Example:**
  >
  > ```jsx
  > function Counter(props) {
  >   return (
  >     <div>
  >       <p>You clicked {props.count} times</p>
  >       <button onClick={props.onIncrement}>Click me</button>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Further Resources:**
  >
  > - React Documentation (Props):
  >
  > [Passing Props to a Component – React](https://react.dev/learn/passing-props-to-a-component)
- **State**
  > **Overview:**
  >
  > - **Focus:** Internal data managed by a component that can change over time.
  > - **Mutable:** Can be updated using methods like `setState` within the component.
  >   **Why use State:**
  >
  > - **Dynamic UI:** Allows components to update their UI based on changes in internal data.
  > - **User Interaction:** Enables components to respond to user actions and update their state accordingly.
  >   **When to use State:**
  >
  > - Managing data that needs to be updated within a component based on user interactions or other events.
  > - Storing temporary data specific to a component.
  >   **Example:**
  >
  > ```jsx
  > function Counter() {
  >   const [count, setCount] = useState(0);
  >
  >   return (
  >     <div>
  >       <p>You clicked {count} times</p>
  >       <button onClick={() => setCount(count + 1)}>Click me</button>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Further Resources:**
  >
  > - React Documentation (State):
  >
  > [State: A Component's Memory – React](https://react.dev/learn/state-a-components-memory)
- **Conditional Rendering**
  > **Focus:** Dynamically controlling which UI elements are rendered based on certain conditions.
  > **Why Use It:**
  >
  > - **Flexible UI:** Enables rendering of different content based on data, state, or user interactions.
  > - **Improved User Experience:** Allows tailoring the UI to specific situations, enhancing user engagement.
  >   **When to Use:**
  >
  > - Displaying content conditionally based on available data.
  > - Implementing interactive controls that affect the UI.
  > - Creating dynamic UIs that respond to user actions.
  >   **Methods:**
  >
  > - **`if` Statements:** Traditional JavaScript `if` statements can be used within JSX to control rendering.
  > - **Ternary Operator:** The concise ternary operator can be used for simple conditional expressions.
  > - **Logical AND Operator (&&):** A shortcut for conditionally rendering elements based on a truthy value.
  >   **Example:**
  >
  > ```jsx
  > function Greeting(props) {
  >   const isLoggedIn = true; // Example state
  >
  >   if (isLoggedIn) {
  >     return (
  >       <div>
  >         <h1>Welcome back, {props.name}!</h1>
  >       </div>
  >     );
  >   } else {
  >     return (
  >       <div>
  >         <p>Please log in.</p>
  >       </div>
  >     );
  >   }
  > }
  > ```
  >
  > **Additional Notes:**
  >
  > - Conditional rendering is often combined with state management techniques (like `useState` or Redux) to manage the conditions that determine what gets rendered.
  > - React hooks like `useState` and `useEffect` provide convenient ways to manage state and trigger conditional re-renders.
  >   **Further Resources:**
  >
  > - React Documentation:
  >
  > [Conditional Rendering – React](https://react.dev/learn/conditional-rendering)
- **Compositions**
  > **Focus:** Building complex UIs by combining smaller, reusable components.
  > **Why Use It:**
  >
  > - **Modularization:** Breaks down complex UIs into manageable and reusable parts.
  > - **Code Maintainability:** Easier to understand, test, and modify individual components.
  > - **Improved Reusability:** Components can be used in multiple parts of the application.
  >   **When to Use:**
  >
  > - When building complex UIs that can be decomposed into smaller, well-defined units.
  > - To promote code reusability and reduce redundancy.
  > - To improve the organization and maintainability of a React application.
  >   **Mechanisms:**
  >
  > - **Props:** Components can pass data (props) to their children, enabling customization and data flow.
  > - **Nesting:** Components can be nested within other components to create hierarchical UI structures.
  > - **Higher-Order Components (HOCs):** Functions that take a component and return a new component with additional functionality (advanced technique).
  >   **Example:**
  >
  > ```jsx
  > function Button(props) {
  >   return <button onClick={props.onClick}>{props.children}</button>;
  > }
  >
  > function Form(props) {
  >   return (
  >     <div>
  >       <input type="text" placeholder="Enter your name" />
  >       <Button onClick={props.onSubmit}>Submit</Button>
  >     </div>
  >   );
  > }
  >
  > function App() {
  >   const handleSubmit = (event) => {
  >     event.preventDefault();
  >     // Handle form submission logic
  >   };
  >
  >   return (
  >     <div>
  >       <Form onSubmit={handleSubmit} />
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Notes:**
  >
  > - Component composition is a fundamental principle in React development, enabling the creation of large and scalable applications.
  > - By using well-defined and reusable components, developers can focus on building specific functionalities without duplicating code.
  >   **Further Resources:**
  >
  > - React Documentation:
  >
  > [Coding Ninjas Studio](https://www.codingninjas.com/studio/library/difference-between-composition-and-inheritance-in-react)

---

# Rendering

In React, rendering refers to the process of transforming your component's code (including JSX) into a viewable HTML structure that gets displayed on the screen. Here are some of the important concepts to understand rendering concepts:

- **Component Life Cycle**
  > **Focus:** The different stages a component goes through during its existence in the application.
  > **Mounting:**
  >
  > - **Description:** The component is first created and inserted into the DOM (Document Object Model).
  > - **Methods:**
  >
  >   - `constructor` (Optional): Used for initialization tasks like binding event handlers.
  >   - `getDerivedStateFromProps` (Optional): Allows updating state based on incoming props (rarely used).
  >   - `render`: Returns the JSX that defines the component's UI.
  >   - `componentDidMount`: Invoked immediately after the component is inserted into the DOM, ideal for side effects like data fetching or subscriptions.
  >     **Updating:**
  >
  > - **Description:** The component updates when its props or state change, triggering a re-render.
  > - **Method:**
  >
  >   - `shouldComponentUpdate` (Optional): Controls whether a re-render should occur based on the updated props and state (often used for performance optimization).
  >   - `render`: Re-executed to reflect the updated state or props in the UI.
  >     **Unmounting:**
  >
  > - **Description:** The component is removed from the DOM.
  > - **Method:**
  >   - `componentWillUnmount`: Invoked immediately before the component is unmounted, useful for cleaning up resources like subscriptions or timers.
  >     **Example:**
  >
  > ```jsx
  > class Counter extends React.Component {
  >   constructor(props) {
  >     super(props);
  >     this.state = { count: 0 };
  >   }
  >
  >   componentDidMount() {
  >     console.log("Component mounted!");
  >   }
  >
  >   handleClick = () => {
  >     this.setState({ count: this.state.count + 1 });
  >   };
  >
  >   render() {
  >     return (
  >       <div>
  >         <p>You clicked {this.state.count} times</p>
  >         <button onClick={this.handleClick}>Click me</button>
  >       </div>
  >     );
  >   }
  > }
  > ```
  >
  > **Additional Notes:**
  >
  > - Understanding the component lifecycle is crucial for managing the state and behavior of components throughout their existence.
  > - Lifecycle methods provide hooks for performing specific actions at different stages.
  > - React provides additional lifecycle methods for handling specific scenarios (e.g., `getSnapshotBeforeUpdate`, `componentDidUpdate`).
  >   **Further Resources:**
  >
  > - React Documentation:
  >
  > [React Component Lifecycle Methods – Explained with Examples](https://www.freecodecamp.org/news/react-component-lifecycle-methods/)
- **List and Props**
  > **Lists:** Represent collections of data items that need to be displayed as an ordered sequence.
  > **Props:** Mechanism for passing data from parent components to their child components.
  > **Relationship:**
  >
  > - **Props within Lists:** Individual list items can be components that receive props to customize their appearance or behavior.
  >   **Why Use Lists:**
  >
  > - **Displaying Collections:** Efficiently render arrays or other data structures containing multiple items.
  > - **Dynamic Content:** Lists can be dynamically populated based on data received from APIs or managed within the application.
  >   **Key Concepts:**
  >
  > - **`map` Function:** A common method for iterating over an array and creating corresponding JSX elements for each item.
  > - **Keys:** Unique identifiers for each list item, crucial for performance optimization and React's reconciliation process.
  >   **Example:**
  >
  > ```jsx
  > import React from "react";
  >
  > function UserList(props) {
  >   return (
  >     <ul>
  >       {props.users.map((user) => (
  >         <li key={user.id}>
  >           {user.name} ({user.email})
  >         </li>
  >       ))}
  >     </ul>
  >   );
  > }
  >
  > function App() {
  >   const users = [
  >     { id: 1, name: "Alice", email: "alice@example.com" },
  >     { id: 2, name: "Bob", email: "bob@example.com" },
  >   ];
  >
  >   return (
  >     <div>
  >       <UserList users={users} />
  >     </div>
  >   );
  > }
  > ```
  >
  > **Further Resources:**
  >
  > - React Documentation (Lists and Keys):
  >
  > [Lists and Keys – React](https://legacy.reactjs.org/docs/lists-and-keys.html)
- **Render props**
  > **Focus:** A technique for sharing code between React components using a prop that is a function.
  > **Purpose:** Allows child components to define the rendering logic based on the data or state provided by the parent component.
  > **Why Use Them:**
  >
  > - **Component Reusability:** Enables creating generic components that can be customized for different rendering needs.
  > - **Code Abstraction:** Hides the implementation details of child components from the parent, promoting separation of concerns.
  >   **When to Use:**
  >
  > - When the rendering logic needs to be dynamic and dependent on data or state managed by the parent component.
  > - For creating reusable components that provide a flexible way to customize their appearance or behavior.
  >   **How It Works:**
  >
  > 1. **Parent Component:**
  >    - Passes a function as a prop (often named `render`) to the child component.
  >    - This function typically receives data or state values from the parent.
  > 2. **Child Component:**
  >    - Receives the `render` prop as an argument.
  >    - Uses the provided data or state within the `render` function to define the UI elements to be displayed.
  >      **Example:**
  >
  > ```jsx
  > function FancyButton(props) {
  >   return (
  >     <button onClick={props.onClick}>
  >       {props.render ? props.render("Click me!") : "Click me!"}
  >     </button>
  >   );
  > }
  >
  > function App() {
  >   const [count, setCount] = useState(0);
  >
  >   const handleClick = () => setCount(count + 1);
  >
  >   return (
  >     <div>
  >       <FancyButton
  >         onClick={handleClick}
  >         render={(message) => (
  >           <span>
  >             {message} ({count})
  >           </span>
  >         )}
  >       />
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Notes:**
  >
  > - While render props offer flexibility, they can sometimes lead to increased code complexity compared to traditional prop drilling or state management solutions.
  > - In modern React development, custom hooks are often preferred over render props for managing complex logic and state within components.
  >   **Further Resources:**
  >
  > - React Legacy Documentation (Render Props):
  >
  > [Render Props – React](https://legacy.reactjs.org/docs/render-props.html)
  >
  > - Article on Render Props vs. Custom Hooks:
  >   [React render props vs. custom Hooks - LogRocket Blog](https://blog.logrocket.com/react-render-props-vs-custom-hooks/)
- **Refs**
  > **Focus:** A way to access DOM elements or React component instances directly.
  > **Why Use Them:**
  >
  > - **Direct DOM Manipulation:** Useful for situations where state and props alone are insufficient (e.g., focusing an input element, integrating with third-party DOM libraries).
  > - **Manual Measurements:** Can be used to access element dimensions or perform manual DOM manipulations.
  >   **When to Use Refs:**
  >
  > - **Focus Management:** Programmatically focusing or blurring form elements.
  > - **Accessing DOM Nodes:** Working directly with DOM elements outside of React's rendering process (rarely used).
  > - **Integrating with Third-Party Libraries:** Interacting with libraries that rely on DOM manipulation.
  >   **Types of Refs:**
  >
  > 1. **String Refs (Legacy):** Deprecated approach where a ref is a string attached to a DOM element using a `ref` attribute.
  > 2. **Callback Refs:** Modern and preferred way where a ref is a function that receives the underlying DOM element or React component instance as an argument.
  >    **Example (Callback Ref):**
  >
  > ```jsx
  > import React, { useRef } from "react";
  >
  > function InputRef() {
  >   const inputRef = useRef(null);
  >
  >   const focusInput = () => {
  >     if (inputRef.current) {
  >       inputRef.current.focus();
  >     }
  >   };
  >
  >   return (
  >     <div>
  >       <input type="text" ref={inputRef} />
  >       <button onClick={focusInput}>Focus Input</button>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Notes:**
  >
  > - Refs provide an "escape hatch" from React's declarative rendering model, allowing for imperative DOM manipulation when necessary.
  > - Use refs judiciously, as over-reliance can lead to less predictable and maintainable code. In many cases, state management or custom hooks might offer better solutions.
  >   **Further Resources:**
  >
  > React Documentation (Refs and the DOM):
  >
  > [Referencing Values with Refs – React](https://react.dev/learn/referencing-values-with-refs)
- **Events**
  > **Focus:** Handling user interactions and system-generated events within React components.
  > **Why Use Them:**
  >
  > - **Interactive UIs:** Respond to user actions like clicks, key presses, form submissions, etc.
  > - **Dynamic Behavior:** Update the UI or trigger side effects based on user interactions.
  >   **Event Handlers:**
  >
  > - **Inline Functions:** Functions defined directly within JSX and passed as props (often used for simple event handling).
  > - **Separate Functions:** Functions defined outside of JSX and called within event handler attributes for better organization and reusability.
  >   **Synthetic Events:**
  >
  > - React creates its own cross-browser wrapper events called Synthetic Events, ensuring consistent behavior across different browsers.
  >   **Common Event Types:**
  >
  > - `onClick`: Click event on an element.
  > - `onChange`: Change event for form elements (e.g., input, text-area).
  > - `onSubmit`: Submission event for forms.
  > - `onFocus`: Focus event on an element.
  > - `onBlur`: Blur event when focus leaves an element.
  > - And many more...
  >   **Preventing Default Behavior:**
  >
  > - You can use `event.preventDefault()` to prevent the default behavior associated with an event (e.g., preventing form submission on button click).
  >   **Example:**
  >
  > ```jsx
  > function Button(props) {
  >   const handleClick = (event) => {
  >     event.preventDefault(); // Prevent default form submission if applicable
  >     console.log("Button clicked!");
  >     props.onClick && props.onClick(event); // Call custom click handler if provided
  >   };
  >
  >   return <button onClick={handleClick}>Click me</button>;
  > }
  > ```
  >
  > **Additional Notes:**
  >
  > - Event handlers can access event information using the `event` object passed as an argument. This object contains properties like `target` (the element that triggered the event) and details specific to the event type.
  > - React supports event bubbling, where events propagate up the component hierarchy unless explicitly stopped.
  >   **Further Resources:**
  >
  > - React Documentation (Handling Events): [https://reactjs.org/docs/handling-events.html](https://reactjs.org/docs/handling-events.html)
- **High Order Functions and Components**
  > **Overview:** In the context of React, Higher-Order Components (HOCs) are a design pattern, not a built-in React feature. However, they leverage higher-order functions, which are a core JavaScript concept.
  > $**Higher-Order Functions (JavaScript)**$ > **Focus:** Functions that take a function as an argument and either return a new function or another value based on the provided function.
  > **Why Use Them:**
  >
  > - **Abstraction:** Encapsulate common functionality and logic within reusable functions.
  > - **Code Reusability:** Promote writing generic functions that can operate on other functions.
  > - **Currying:** Create new functions with partially applied arguments (advanced technique).
  >   **Examples:**
  >
  > 1. **`map` function:** Takes an array and a function as arguments, applies the function to each element in the array, and returns a new array with the results.
  > 2. **`filter` function:** Takes an array and a function as arguments, filters the array based on the function's return value (true for inclusion, false for exclusion), and returns a new array with the filtered elements.
  >    $**Higher-Order Components (React)**$ > **Focus:** Functions that take a React component as an argument and return a new component that wraps the original component, potentially adding additional functionality or behavior.
  >    **Why Use Them:**
  >
  > - **Code Reusability:** Share common functionalities (e.g., authentication, logging) across different components without code duplication.
  > - **Separation of Concerns:** Decouple core component logic from concerns like authentication or state management.
  > - **Component Composition:** Create more complex components by combining simpler ones with HOCs.
  >   **Example:**
  >
  > ```jsx
  > function withAuthentication(WrappedComponent) {
  >   return (props) => {
  >     const isAuthenticated = true; // Simulate authentication state
  >
  >     return (
  >       <div>
  >         {isAuthenticated ? (
  >           <WrappedComponent {...props} />
  >         ) : (
  >           <p>Please log in to access this content.</p>
  >         )}
  >       </div>
  >     );
  >   };
  > }
  >
  > function MyComponent(props) {
  >   return (
  >     <div>
  >       <h1>Welcome, {props.name}!</h1>
  >       <p>This is protected content.</p>
  >     </div>
  >   );
  > }
  >
  > const AuthProtectedComponent = withAuthentication(MyComponent);
  >
  > // Usage
  > <AuthProtectedComponent name="John" />;
  > ```
  >
  > **Additional Notes:**
  >
  > - HOCs can accept additional arguments to customize their behavior.
  > - While HOCs offer benefits, overuse can lead to complex component hierarchies. Consider alternatives like custom hooks or render props in modern React development.
  >   **Further Resources:**
  >
  > - Higher-Order Functions in JavaScript:
  >
  > [First-class Function - MDN Web Docs Glossary: Definitions of Web-related terms | MDN](https://developer.mozilla.org/en-US/docs/Glossary/First-class_Function)
  >
  > - Higher-Order Components in React (freeCodeCamp):
  >
  > [How to use React’s higher-order components](https://www.freecodecamp.org/news/react-higher-order-components-635d0bc38b6c/)

---

# Hooks

In React, hooks are functions introduced in React 16.8 that allow you to "hook into" React state and lifecycle features from functional components. Some of the commonly used hooks are listed below:

- **useState**
  > **Overview:** The `useState` Hook in React provides a built-in mechanism for managing component state within functional components, facilitating the creation of dynamic and stateful user interfaces efficiently.
  > **What is State?**
  >
  > - Component state represents internal data managed by a component that can change over time.
  > - Changes in state trigger re-renders of the component, ensuring the UI reflects the latest state values.
  >   **Usage:**
  >
  > 1. **Import:** Import the `useState` Hook from React at the top of your functional component file.
  >
  > ```jsx
  > import React, { useState } from "react";
  > ```
  >
  > 1. **Calling the Hook:** Inside your functional component, call the `useState` Hook. It takes an initial state value (often null, an empty array, or an empty object) as an argument and returns an array with two elements:
  >    - **Current State:** The current value of the state variable.
  >    - **State Setter Function:** A function used to update the state.
  >      **Example:**
  >
  > ```jsx
  > import React, { useState } from "react";
  >
  > function Counter() {
  >   // Call useState with initial state (0)
  >   const [count, setCount] = useState(0);
  >
  >   const handleClick = () => {
  >     // Update state using the setter function
  >     setCount(count + 1);
  >   };
  >
  >   return (
  >     <div>
  >       <p>You clicked {count} times</p>
  >       <button onClick={handleClick}>Click me</button>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - Functional state updates using the setter function guarantee predictable state updates and prevent potential errors.
  > - You can call `useState` multiple times within a component to manage multiple state variables independently.
  >   **Further Resources:**
  >
  > - React Hooks Documentation (`useState`):
  >
  > [useState – React](https://react.dev/reference/react/useState)
- **useEffect**
  > **Overview:** The `useEffect` Hook in React enables functional components to handle side effects, such as data fetching or DOM manipulation, effectively. By utilizing its dependency array, you can optimize performance by controlling when effects are executed.
  > **What are Side Effects?**
  >
  > Side effects are operations that interact with external systems or have other impacts outside of the component itself. Examples include:
  >
  > - Data fetching (from APIs or local storage)
  > - Subscriptions (to events or data sources)
  > - Manual DOM manipulations (use sparingly)
  > - Timers (for scheduling actions)
  >   **Why Use `useEffect`?**
  >
  > - **Functional Component Suitability:** Enables side effects within functional components, previously only possible with lifecycle methods in class components.
  > - **Controlled Execution:** Allows you to specify when and how side effects should run.
  >   **Using `useEffect`:**
  >
  > 1. **Import:** Import the `useEffect` Hook from React at the top of your functional component file.
  >
  >    **JavaScript**
  >
  >    ```jsx
  >    import React, { useEffect } from "react";
  >    ```
  >
  > 2. **Calling the Hook:** Call the `useEffect` Hook inside your functional component. It takes a callback function (the effect) and an optional dependency array as arguments.
  >    **The Effect Function:**
  >
  > - This function defines the actual side effect logic that you want to execute.
  > - It can access the component's props and state using the hook's arguments or closure.
  >   **Dependency Array (Optional):**
  >
  > - An optional array of dependencies specifies when the effect should re-run. The effect runs again whenever any of the dependencies in the array change.
  > - If no dependency array is provided, the effect runs after every render (similar to `componentDidMount` in class components).
  >   **Example (Fetching Data on Mount):**
  >
  > ```jsx
  > import React, { useEffect } from "react";
  >
  > function UserList() {
  >   const [users, setUsers] = useState([]);
  >
  >   useEffect(() => {
  >     const fetchUsers = async () => {
  >       const response = await fetch("https://api.example.com/users");
  >       const data = await response.json();
  >       setUsers(data);
  >     };
  >
  >     fetchUsers();
  >   }, []); // Empty dependency array: run only on mount
  >
  >   return (
  >     <ul>
  >       {users.map((user) => (
  >         <li key={user.id}>{user.name}</li>
  >       ))}
  >     </ul>
  >   );
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - The effect function can optionally return a cleanup function that runs before the component unmounts or before the effect runs again due to a dependency change. This is useful for cleaning up subscriptions, timers, or other side effects that should be stopped.
  > - Use `useEffect` judiciously, as excessive side effects can impact performance. Consider alternatives like derived state or custom hooks for complex logic.
  >   **Further Resources:**
  >
  > - React Hooks Documentation (`useEffect`):
  >
  > [useEffect – React](https://react.dev/reference/react/useEffect)
- **useContext**
  > **Overview:** The `useContext` Hook in React enables functional components to access context values provided by a `React.createContext` provider component, facilitating data sharing across components without prop drilling. It enhances component organization and reusability, but should be used judiciously for suitable scenarios.
  > **Context in React:**
  >
  > - A mechanism for managing and sharing data across components in a React application without explicitly passing props down through the component tree (prop drilling).
  > - Established using `React.createContext` which returns a context object.
  >   **Using `useContext`:**
  >
  > 1. **Import:** Import `useContext` from React at the top of your functional component file.
  >
  >    ```jsx
  >    import React, { useContext } from "react";
  >    ```
  >
  > 2. **Calling the Hook:** Call the `useContext` Hook within your functional component. It takes the context object (created with `React.createContext`) as an argument.
  >    **Example:**
  >
  > **1. Creating the Context:**
  >
  > ```jsx
  > const ThemeContext = React.createContext("light"); // Default theme
  > ```
  >
  > **2. Providing the Context:**
  >
  > ```jsx
  > import React, { useContext } from "react";
  >
  > function App() {
  >   const [theme, setTheme] = useState("light");
  >
  >   const toggleTheme = () => {
  >     setTheme(theme === "light" ? "dark" : "light");
  >   };
  >
  >   return (
  >     <ThemeContext.Provider value={theme}>
  >       <Toolbar toggleTheme={toggleTheme} />
  >       <Content />
  >     </ThemeContext.Provider>
  >   );
  > }
  > ```
  >
  > **3. Consuming the Context (using `useContext`):**
  >
  > ```jsx
  > function Toolbar(props) {
  >   const theme = useContext(ThemeContext); // Access the context value
  >
  >   return (
  >     <button onClick={props.toggleTheme}>Toggle Theme ({theme})</button>
  >   );
  > }
  >
  > function Content() {
  >   const theme = useContext(ThemeContext); // Access the context value
  >
  >   return (
  >     <div style={{ backgroundColor: theme === "light" ? "white" : "black" }}>
  >       Content with theme: {theme}
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - Context updates trigger re-renders in all consumer components that use `useContext`. Optimize context usage to avoid unnecessary re-renders.
  > - Consider alternatives like `Redux` or `Zustand` for complex global state management needs.
  >   **Further Resources:**
  >
  > - React Hooks Documentation (`useContext`):
  >
  > [useContext – React](https://react.dev/reference/react/useContext)
- **useReducer**
  > **Overview:** The `useReducer` Hook in React facilitates the management of complex state logic within functional components by employing a reducer function. It promotes structured and predictable state updates, enhancing code readability and maintainability.
  > **What is a Reducer?**
  >
  > - A reducer function is a pure function that takes the current state and an action object as arguments, and returns a new state based on the action type and payload.
  >   **Why Use `useReducer`?**
  >
  > - **Complex State Management:** Suitable for managing intricate state logic involving multiple state values or interdependent updates.
  > - **Improved Readability:** Separates state update logic from the component, promoting cleaner and more maintainable code.
  > - **Performance Optimization:** Can potentially optimize performance in complex state scenarios by calculating minimal state updates.
  >   **Using `useReducer`:**
  >
  > 1. **Import:** Import `useReducer` from React at the top of your functional component file.
  >
  >    ```jsx
  >    import React, { useReducer } from "react";
  >    ```
  >
  > 2. **Calling the Hook:** Call `useReducer` within your functional component. It takes two arguments:
  >    - **Reducer Function:** The function that defines how the state should be updated based on actions.
  >    - **Initial State:** The initial value of the state object.
  >      **Example:**
  >
  > ```jsx
  > import React, { useReducer } from "react";
  >
  > function Counter() {
  >   const initialState = { count: 0 };
  >
  >   const reducer = (state, action) => {
  >     switch (action.type) {
  >       case "increment":
  >         return { count: state.count + 1 };
  >       case "decrement":
  >         return { count: state.count - 1 };
  >       default:
  >         return state;
  >     }
  >   };
  >
  >   const [state, dispatch] = useReducer(reducer, initialState);
  >
  >   const handleClick = (type) => {
  >     dispatch({ type }); // Dispatch actions to update state
  >   };
  >
  >   return (
  >     <div>
  >       <p>You clicked {state.count} times</p>
  >       <button onClick={() => handleClick("increment")}>Increment</button>
  >       <button onClick={() => handleClick("decrement")}>Decrement</button>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - Reducers are pure functions, ensuring predictable state updates based on the previous state and the dispatched action.
  > - You can combine `useReducer` with `useMemo` to optimize performance by memoizing the reducer function or parts of the state that don't need to be recalculated on every render.
  >   **Further Resources:**
  >
  > - React Hooks Documentation (`useReducer`):
  >
  > [useReducer – React](https://react.dev/reference/react/useReducer)
- **useCallback**
  > **Overview:** The `useCallback` Hook in React optimizes performance by memoizing callback functions within functional components, ensuring stable references and minimizing unnecessary re-renders of child components.
  > **Why Use `useCallback`?**
  >
  > - **Performance Optimization:** Prevents expensive function recreations on every render, especially when passed as props to child components.
  > - **Reference Equality Checks:** Ensures child components only re-render if the reference (memory location) of the callback function has actually changed, not just its content.
  >   **When to Use `useCallback`:**
  >
  > - Commonly used for callback functions passed as props to child components, especially when those functions rely on the component's state or props.
  > - Can also be used for memoizing expensive calculations or functions used within event handlers to avoid redundant computations.
  >   **Using `useCallback`:**
  >
  > 1. **Import:** Import `useCallback` from React at the top of your functional component file.
  >
  >    ```jsx
  >    import React, { useCallback } from "react";
  >    ```
  >
  > 2. **Calling the Hook:** Call `useCallback` within your functional component. It takes two arguments:
  >    - **Callback Function:** The function you want to memoize.
  >    - **Dependency Array (Optional):** An optional array of dependencies that determine when the memoized function should be recreated. If no dependency array is provided, the memoized function will only be created once.
  >      **Example:**
  >
  > ```jsx
  > import React, { useCallback } from "react";
  >
  > function MyComponent(props) {
  >   const [count, setCount] = useState(0);
  >
  >   const handleClick = useCallback(() => {
  >     console.log("Button clicked! Count:", count);
  >   }, [count]); // Recreates handleClick only when count changes
  >
  >   return (
  >     <div>
  >       <p>Count: {count}</p>
  >       <button onClick={handleClick}>Click me</button>
  >       <ChildComponent handleClick={handleClick} />
  >     </div>
  >   );
  > }
  >
  > function ChildComponent(props) {
  >   // handleClick will only be recreated in MyComponent when count changes
  >   // due to useCallback in MyComponent
  >   return <button onClick={props.handleClick}>Click from Child</button>;
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - `useMemo` is a similar hook that can be used to memoize the result of any value based on its dependencies. However, `useCallback` specifically returns a memoized function.
  > - Use `useCallback` judiciously, as excessive memoization can add complexity. Only memoize functions that are truly expensive to create or cause unnecessary re-renders in child components.
  >   **Further Resources:**
  >
  > - React Hooks Documentation (`useCallback`):
  >
  > [useCallback – React](https://react.dev/reference/react/useCallback)
- **useRef**
  > **Overview:** The `useRef` Hook in React allows you to create mutable reference objects ("refs") within functional components, capable of holding values like DOM elements or other data that persist across renders. While useful for certain scenarios, it's important to exercise caution and prioritize declarative UI updates with `state` and `JSX` whenever feasible.
  > **Why Use `useRef`?**
  >
  > - **Direct DOM Access (Limited Use):** In rare cases, you might need to directly access or manipulate a DOM element from a functional component. Refs provide a way to store a reference to the DOM element.
  > - **Storing Mutable Values:** While state updates trigger re-renders, refs can hold mutable values that don't cause re-renders, useful for storing previous values or references across renders.
  > - **Focus Management:** You can use refs to manage focus on form elements or other interactive components.
  >   **Use Cases (Use with Caution):**
  >
  > - **Direct DOM manipulation (rarely recommended):** Due to potential performance issues and separation of concerns principles, it's generally recommended to handle UI updates declaratively using state and JSX.
  > - **Measuring DOM elements:** You can use a ref to store a DOM element and access its properties (e.g., width, height) later in your component.
  > - **Focus management:** Refs can be attached to form elements to programmatically focus or blur them.
  >   **Using `useRef`:**
  >
  > 1. **Import:** Import `useRef` from React at the top of your functional component file.
  >
  >    ```jsx
  >    import React, { useRef } from "react";
  >    ```
  >
  > 2. **Calling the Hook:** Call `useRef` within your functional component. It returns a new ref object with a single property:
  >    - `.current`: Initially set to the value passed to `useRef` (often null or an empty object). You can assign values to `.current` later.
  >      **Example (Focusing an Input):**
  >
  > ```jsx
  > import React, { useRef } from "react";
  >
  > function TextInput() {
  >   const inputRef = useRef(null);
  >
  >   const focusInput = () => {
  >     if (inputRef.current) {
  >       inputRef.current.focus();
  >     }
  >   };
  >
  >   return (
  >     <div>
  >       <input ref={inputRef} type="text" />
  >       <button onClick={focusInput}>Focus Input</button>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - Unlike state updates, changes to a ref's `.current` property won't trigger a re-render.
  > - Use refs cautiously for side effects or integrating with third-party libraries that rely on imperative DOM manipulation.
  >   **Further Resources:**
  >
  > - React Hooks Documentation (`useRef`):
  >
  > [useRef – React](https://react.dev/reference/react/useRef)
- **useMemo**
  > **Overview:** The `useMemo` Hook in React empowers you to optimize performance by memoizing the results of calculations or function calls within functional components. It ensures that these values are only recalculated when their dependencies change, leading to a more efficient and responsive user experience.
  > **Why Use `useMemo`?**
  >
  > - **Performance Optimization:** Prevents redundant calculations within components, especially when dealing with complex computations or data transformations.
  > - **Improved Efficiency:** Ensures the memoized value is only recalculated when its dependencies change, leading to smoother performance.
  >   **When to Use `useMemo`:**
  >
  > - Frequently used for memoizing expensive calculations or function calls that rely on the component's state or props.
  > - Can also be used to create derived data based on other state or props, preventing redundant computations on every render.
  >   **Using `useMemo`:**
  >
  > 1. **Import:** Import `useMemo` from React at the top of your functional component file.
  >
  >    **JavaScript**
  >
  >    ```jsx
  >    import React, { useMemo } from "react";
  >    ```
  >
  > 2. **Calling the Hook:** Call `useMemo` within your component. It takes two arguments:
  >    - **Calculation Function:** The function whose result you want to memoize.
  >    - **Dependency Array (Optional):** An array of values that the calculation depends on. If a dependency in the array changes, the memoized value will be recalculated. If no dependency array is provided, the value will be recalculated on every render.
  >      **Example (Memoizing a Complex Calculation):**
  >
  > ```jsx
  > import React, { useMemo } from "react";
  >
  > function ExpensiveComponent(props) {
  >   const [data, setData] = useState([]);
  >
  >   const calculateAverage = useMemo(() => {
  >     if (!data.length) return 0;
  >
  >     const sum = data.reduce((acc, val) => acc + val, 0);
  >     return sum / data.length;
  >   }, [data]); // Recalculate only when data changes
  >
  >   return (
  >     <div>
  >       <p>Average: {calculateAverage}</p>
  >       <button onClick={() => setData([...data, Math.random()])}>
  >         Add Data
  >       </button>
  >     </div>
  >   );
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - `useCallback` is a similar hook used for memoizing callback functions specifically.
  > - Use `useMemo` judiciously, as excessive memoization can add complexity. Only memoize values that are truly expensive to calculate and cause performance issues if recalculated frequently.
  >   **Further Resources:**
  >
  > - React Hooks Documentation (`useMemo`):
  >
  > [useMemo – React](https://react.dev/reference/react/useMemo)
- **custom hooks**
  > **Overview:** `Custom hooks` in React are reusable functions designed to encapsulate stateful logic or side effects, following the naming convention of starting with "use" (e.g., useForm, useFetch). They enhance code reusability, improve component organization, and enable the creation of modular and maintainable React applications.
  > **Why Use `Custom Hooks`?**
  >
  > - **Code Reusability:** Custom hooks promote code reuse by encapsulating common functionalities that can be shared across multiple components.
  > - **Improved Organization:** They break down complex logic into smaller, more manageable units, enhancing code readability and maintainability.
  > - **State Management Abstraction:** Custom hooks can manage state logic for specific use cases, separating concerns and improving component clarity.
  >   **Creating `Custom Hooks`:**
  >
  > 1. **Functionality:** Define the functionality you want to encapsulate in the hook. This could involve state management using `useState` or side effects with `useEffect`.
  > 2. **Logic:** Implement the logic using React hooks and other JavaScript functionalities within the custom hook function.
  >    **Using `Custom Hooks`:**
  >
  > 3. **Import:** Import the custom hook file into the component where you want to use it.
  > 4. **Call the Hook:** Call the custom hook function within your component, similar to how you use built-in hooks like `useState` or `useEffect`. The custom hook can return values or provide functions for managing state or side effects.
  >    **Example (Custom Hook for Form Handling):**
  >
  > **`useForm.js` (Custom Hook File):**
  >
  > ```jsx
  > import { useState } from "react";
  >
  > function useForm(initialState) {
  >   const [values, setValues] = useState(initialState);
  >
  >   const handleChange = (event) => {
  >     setValues({ ...values, [event.target.name]: event.target.value });
  >   };
  >
  >   return { values, handleChange };
  > }
  >
  > export default useForm;
  > ```
  >
  > **`MyForm.js` (Component Using the Hook):**
  >
  > ```jsx
  > import React from "react";
  > import useForm from "./useForm";
  >
  > function MyForm() {
  >   const { values, handleChange } = useForm({ name: "", email: "" });
  >
  >   const handleSubmit = (event) => {
  >     event.preventDefault();
  >     console.log("Form submitted:", values);
  >   };
  >
  >   return (
  >     <form onSubmit={handleSubmit}>
  >       <label>
  >         Name:
  >         <input
  >           type="text"
  >           name="name"
  >           value={values.name}
  >           onChange={handleChange}
  >         />
  >       </label>
  >       <label>
  >         Email:
  >         <input
  >           type="email"
  >           name="email"
  >           value={values.email}
  >           onChange={handleChange}
  >         />
  >       </label>
  >       <button type="submit">Submit</button>
  >     </form>
  >   );
  > }
  > ```
  >
  > **Additional Considerations:**
  >
  > - Custom hooks can accept arguments to customize their behavior (e.g., initial state for `useForm`).
  > - They can return multiple values or functions depending on the encapsulated logic.
  > - Use custom hooks strategically to avoid over-engineering or creating unnecessary abstractions.
  >   **Further Resources:**
  >
  > - React Hooks Documentation:
  >
  > [React Reference Overview – React](https://react.dev/reference/react)

---

# Routing

- React router

---

# State Management

- Zustand

---

# Styling

- Tailwind
- Bootstrap

---

# API calls

1. GraphQL:
   - Apollo
2. REST:
   - React-query

---

# Testing

- JTest
- React Testing Library

---

# Frameworks

- Next.JS
- Vue.JS

---

# Forms

- React Hook Form

---

# Advance Topics

- Suspense
- Portals
- Error Boundaries
- Fiber Architecture

---

# Mobile

- React Native

---
