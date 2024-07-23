# 1.3: React

## Introduction

<a href="https://react.dev" target="_blank">React</a> is a frontend framework and library that allows us to create custom, nest-able UI elements with a combination of HTML and JavaScript syntax (JSX). React's HTML-like structure makes it easy to visualise, and its integrated JS makes it easy to render dynamic data. Alternative but less popular frontend libraries include <a href="https://vuejs.org" target="_blank">Vue</a> and <a href="https://angularjs.org" target="_blank">Angular</a>.

We will use React's official <a href="https://react.dev/learn" target="_blank">guide</a> and <a href="https://react.dev/learn/tutorial-tic-tac-toe" target="_blank">tutorial</a> to learn React, and the <a href="https://vitejs.dev/guide/" target="_blank">Vitejs</a> environment to scaffold our first React apps. Vite is a build tool that provides a fast and lean development experience for modern web projects. Vite leverages new advancements in the JavaScript ecosystems, the ability of native ES modules within the browser and the rise of JavaScript tools written in compile-to-native languages. This is because browsers do not read React natively; they read HTML, CSS and JS, not JSX.&#x20;

The following sections provide Rocket's annotations to React's official <a href="https://react.dev/learn" target="_blank">guide</a> and <a href="https://react.dev/learn/tutorial-tic-tac-toe" target="_blank">tutorial</a> to explain concepts that the React team assumes readers know.



## Day 5



## Day 6



## Using the <a href="https://react.dev/reference/react/useState">`useState`</a> Hook

We will use the `useState` Hook most often. Clear explanations of what the `useState` Hook is and how to use it.

> Rocket strongly recommends following the naming convention of `X` and `setX` as the de-structured state variable names from `useState`. This makes our code more readable because other engineers will immediately know what each variable is for.

### Sample useState Hook

{% include youtube.html id="eb6HKsxHoas" %}
React Hooks useState

### 6: <a href="https://react.dev/learn/managing-state" target="_blank">React State management, useState</a>

While creating your application and enlarging functionalities you will find that you are developing your components and states into much larger and complex files than you had before. IT is important to manage state effectively and reduce redundant or duplicated states within your application.&#x20;

1. When using useState to manage component state Rocket advises following these steps
   1. Import the useState hook from the react package, at the top of the component file
   2. Within your functional component declare a state variable and the updater function using the useState hook. As shown on <a href="https://react.dev/learn/managing-state#reacting-to-input-with-state" target="_blank">line 4</a>.&#x20;
   3. The initialValue of the state is passed into useState.
   4. You can update this variable using the updater function.
2. We will take a longer look onto useContext and useReducer later in this course.
3. When developing your state, group information if two state variables always change together, therefore unify them into a single state variable. Here are some more rules regarding <a href="https://react.dev/learn/choosing-the-state-structure" target="_blank">state structure</a>.
4. When updating a state variable its possible to use its current value, this is done by invoking a callback function on the updater function. Take a look at <a href="https://react.dev/reference/react/useState#updating-state-based-on-the-previous-state" target="_blank">these examples here</a>.

## Using the <a href="https://react.dev/reference/react/useEffect">`useEffect`</a> Hook

At Rocket we will use `useEffect` instead of the lifeCycleMethod `componentDidMount` for setting up subscriptions such as Firebase listeners and for data fetching. `useEffect` also allows us to perform functionality that was previously provided by `componentDidUpdate` and `componentWillUnmount`, but we will use that functionality less often.


1. As the docs mention, we can think of `useEffect` as running after the component renders.
2. A memory leak is when data that we use in parts of our apps is not properly cleaned up after the app stops using those parts. This can cause our apps to run slowly and even crash if the "leaks" cause our computers to run out of memory while running our apps. This will rarely happen to use in practice because JavaScript has automatic memory management and our apps will not be the most complex for now.
3. Returning a cleanup function from `useEffect` is optional and we will not use it often at Rocket.
4. No need to worry too much about "Optimizing Performance by Skipping Effects"; we will rarely need this and we can come back to it once we're more familiar with using `useEffect` and Hooks in general.


### Sample useEffect Hook

{% include youtube.html id="z4eeYjk57aM" %}
React Hooks useEffect

### 7: <a href="https://react.dev/learn/lifecycle-of-reactive-effects" target="_blank">Component LifeCycles</a> & <a href="https://react.dev/learn/synchronizing-with-effects#how-to-write-an-effect" target="_blank">useEffect</a>

While developing React components it is possible to embed executable code within a component that runs on certain conditions. A common and useful pattern developers employ would be to call an API after the Component loads to get some information to display within the application. This can be controlled by the `useEffect` hook that is part of ReactJs.&#x20;

1. Understand a components lifecycle and how they are "mounted", "updated" and "unmounted".
2. In React we use effects to describe how to synchronise  an external system to the current prop and state.&#x20;
3. Understand how useEffect is implemented in components and what are the triggers that will force them to execute code
   1. Import the useEffect hook from the react package, at the top of the component file
   2. Call it at the top level of the component and put in your code, note state updates must be handled using conditional statements
   3. Handle effect with dependencies, inside the dependency array, passed as the second argument to useEffect
   4. Handle any effect clean ups by implemented a cleanup function within the effect.&#x20;
4. <a href="https://react.dev/reference/react/useEffect" target="_blank">React's offical guide and additional reference</a> to the useEffect hook

<!-- ## Post-Class Exercises: Codecademy React 101

Complete all exercises in the following Codecademy lessons when they are assigned in the Rocket course schedule.

1. React Components
   1. <a href="https://www.codecademy.com/courses/react-101/lessons/your-first-react-component/exercises/hello-world-component" target="_blank">Your First React Component</a>
   2. <a href="https://www.codecademy.com/courses/react-101/lessons/react-components-advanced-jsx/exercises/render-multiline-jsx" target="_blank">Components and Advanced JSX</a>
   3. <a href="https://www.codecademy.com/courses/react-101/lessons/components-render-each-other/exercises/components-interacting-intro" target="_blank">Components Render Other Components</a>
   4. <a href="https://www.codecademy.com/courses/react-101/lessons/this-props/exercises/this-props-intro" target="_blank">this.props</a>
2. Hooks
   1. <a href="https://www.codecademy.com/courses/react-101/lessons/stateless-functional-components/exercises/stateless-functional-component-intro" target="_blank">Function Components</a>
   2. <a href="https://www.codecademy.com/courses/react-101/lessons/the-state-hook" target="_blank">The State Hook</a>
   3. <a href="https://www.codecademy.com/courses/react-101/lessons/the-effect-hook/exercises/function-component-effects" target="_blank">The Effect Hook</a> -->

## Additional Resources

The following resources are optional and can be used more for reference than upfront reading.

1. <a href="https://react.dev/learn/reusing-logic-with-custom-hooks" target="_blank">Re-using logic with Custom Hooks</a>
2. <a href="https://react.dev/reference/react" target="_blank">Hooks API Reference</a>

## Day 7

### 8: <a href="https://react.dev/learn/responding-to-events" target="_blank">Handling Events</a>

When users click on a button they expect some result, or some change, take the counter example if you click on the button the state increments. To develop these types of functionality within our React applications we will need to handle events, but assigning an event listener to our elements and define some callback functions to handle the event in a meaningful way. In our JSX code we need to follow these steps to handle events.

1. How do you handle events?
   1. Attach the event listener to the element, such as an `onClick` or `onBlur` event.
   2. Define the callback function that will handle said event, accessing the event data if required. Remember to pass this function to the event handler.&#x20;
   3. Update state within this callback function by calling an updater function, run a side effect or execute any code.
2. "Events on DOM elements" are the same as <a href="https://www.w3schools.com/js/js_events.asp" target="_blank">JavaScript events or HTML events</a>. JS events allow us to perform logic on events that happen on our web pages such as mouse clicks. React supports a <a href="https://react.dev/reference/react-dom/components/common#common-props" target="_blank">wide range of events.</a>
3. Remember that functions that are passed to event handlers must be passed and not called, you can wrap the given function in an anonymous function if you need to pass in arguments.
4. You are able to stop event propagation as well as the default action.



### 7: <a href="https://react.dev/learn/conditional-rendering" target="_blank">Conditional Rendering</a>

Components will often need to display different UI's depending on conditions passed down as props, or the information its processing. You are able to conditionally render JSX in React using various patterns within JavaScript including conditonal statements that return JSX, or <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_operator" target="_blank">ternary operators</a>.

1. Conditional rendering is one of the most powerful features of React, enabling us to use conditional logic to specify what a component should render.
2. You can use inline code for conditionals, `condition ? true : false` syntax is the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator" target="_blank">JavaScript conditional operator</a>.

### 8: <a href="https://react.dev/learn/rendering-lists" target="_blank">Lists and Keys</a>

Lables on cds and JSX keys in an array serve similar purposes, it helps us to identify unique items from thier siblings. Keys help React to identify different JSX elements throughout thier lifetimes. You can generate key values in whatever way you would like, but if you've pulled data out of a database, they might already have identities, such as an Id property. You could create you're own incrementing counter to set unique keys within an application or implement <a href="https://www.npmjs.com/package/uuid" target="_blank">uuid</a> or another packaged that can assign unique id's within an application.&#x20;

1. Rocket recommends always using keys when rendering JSX elements in a list for performance reasons.
2. Keys should be unique among siblings
3. Keys cannot change as that would defeat the purpose of them

## Day 8

### 9: <a href="https://react.dev/reference/react-dom/components#form-components" target="_blank">Forms</a>, <a href="https://react.dev/reference/react-dom/components/input" target="_blank">input</a>, <a href="https://react.dev/reference/react-dom/components/select" target="_blank">select</a>, <a href="https://react.dev/reference/react-dom/components/textarea" target="_blank">textarea</a>

HTML forms and their elements afford developers the opportunity to capture user information as they interact with our application. Forms can be composed of a combination of inputs, selects and textareas, when wrapped in a form tag the values of these inputs can be extracted as form data. Or they can be maintained purely using state. Employ React element such as input, select and text areas to give users different input capabilities.&#x20;

1. An <a href="https://www.w3schools.com/html/html_forms.asp" target="_blank">HTML form</a> is an HTML element that either refreshes the page or navigates to a new page when the user submits the form. We often do not want this behaviour in React, opting to update UI on submit without refresh. To disable "refresh on submit" behaviour, Rocket recommends the technique in the React docs, to provide the `form` a `handleSubmit` callback function that calls `event.preventDefault`.
2. When handling the submit method from a form you should target the `event.target.value` to get the current value of an input.&#x20;
3. You must control the form elements that you use within a React component, do this by passing the value prop to it and handling the associated event. <a href="https://react.dev/reference/react-dom/components/input#controlling-an-input-with-a-state-variable" target="_blank">Have an in-depth look here</a>.&#x20;
4. Note how you will need to create state to capture form data.

<!-- ## Post-Class Exercises: Codecademy React 101&#x20;

Complete all exercises in the following Codecademy lessons when they are assigned in the Rocket course schedule.

1. <a href="https://www.codecademy.com/courses/react-101/lessons/react-forms/exercises/react-forms-intro" target="_blank">React Forms</a> -->



### Day 9

### 10: <a href="https://react.dev/learn/sharing-state-between-components" target="_blank">Lifting State Up</a>

Managing state on components can get challenging and confusing when you need to share data between multiple components.  Especially so while still having to preform live updates and dynamically render content. The process of lifting up state means your children components actually receive data as props. Instead of storing the data on each child, you store the data on a shared parent of both child components. &#x20;

1. It is important that we pass both the temperature value and handle-change function from `Accordian` to `Panel` so the app can maintain only 1 "source of truth" state for the active value in `Panel`. If it helps, Rocket recommends drawing the component hierarchy to visualise how data flows in the application and verifying our understanding with our classmates and section leader.

### Day 10

### 11: <a href="https://react.dev/learn/thinking-in-react" target="_blank">Thinking In React</a>

Developing a user interfaces in React can be challenging. Instead of looking at a webpage as a whole, you should instead split it into sections or components, at this stage we can consider the states required for each component to correctly render as intended. To ensure that data follows correctly you then need to connect your components pass information or functions from parents to children.&#x20;

1. <a href="https://www.w3schools.com/js/js_json_intro.asp" target="_blank">JSON</a> (JavaScript Object Notation) is a data format similar to JavaScript Objects, except can be used in text or file form. An API (Application Programming Interface) is typically a URL that manipulates and/or returns data. A JSON API is an API that returns data in JSON format, one of the most common formats to send and receive data on the internet.
2. Notice the example and how it passes updater function and state from the parent to the child, such that we can control and alter state.

### Day 11

### <a href="https://react.dev/learn/tutorial-tic-tac-toe" target="_blank">Tutorial: Intro to React</a>

If you finish the React Guide pages above early, feel free to start and finish this tutorial early to have more time for [Project 1](../1.p-frontend-app.md).

1. Rocket recommends starting with Setup Option 1 (Write Code in Browser) to focus on understanding React. If you finish the tutorial and have time, do Setup Option 2 (Local Development Environment) and port your code over to understand how to use Create React App. We will use Create React App to develop all frontend projects at Rocket.
2. Rocket recommends using <a href="https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en" target="_blank">React DevTools</a> whenever developing React apps. It can help us debug quicker.
3. Note the tutorial's recommendation to use `on[Event]` naming convention for props that represent events and `handle[Event]` for methods that handle events.

