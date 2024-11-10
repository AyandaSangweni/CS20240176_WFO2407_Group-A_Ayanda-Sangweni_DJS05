# DJS05 Project Brief: Building a Redux-Inspired Store for a Tally App

In this challenge, you will venture into the realm of state management by constructing a Redux-inspired store to manage the state of a simple Tally App. Your primary goal is to manage the app's state changes efficiently, focusing on core functionalities like incrementing, decrementing, and resetting a counter. Instead of rendering changes on the UI, you'll subscribe to state updates and log them to the console, highlighting the power of state management in applications.

## Objective
Create a minimalistic, Redux-inspired store to manage and log the state of a counting Tally App. Your implementation will not involve UI rendering; instead, it will use console logs to demonstrate state management effectively.

Observer Pattern resource from Refactoring Guru: https://refactoring.guru/design-patterns/observer

## User Stories (Gherkin Syntax)
Your challenge will encompass the following scenarios, tested through your store's implementation:

### SCENARIO 1: Initial State Verification
```
GIVEN no interactions have been performed yet
WHEN the “getState” method is run
AND the result is logged to the console
AND the browser console is open
THEN the state should show a count of 0
```

### SCENARIO 2: Incrementing the Counter
```
GIVEN no interactions have been performed yet
WHEN an “ADD” action is dispatched
AND another “ADD” action is dispatched
AND the browser console is open
THEN the state should show a count of 2
```

### SCENARIO 3: Decrementing the Counter
```
GIVEN the current count in the state is 2
WHEN a “SUBTRACT” action is dispatched
AND the browser console is open
THEN the state should display a count of 1
```

### SCENARIO 4: Resetting the Counter
```
GIVEN the current count in the state is 1
WHEN a “RESET” action is dispatched
AND the browser console is open
THEN the state should display a count of 0
```

## Requirements
- **Implement a Global Store**: Create a Redux-inspired store that holds the state of the tally counter. The store should have the ability to dispatch actions and subscribe to state changes.
- **State Management Functions**:
  - **getState**: Returns the current state.
  - **dispatch**: Takes an action (e.g., ADD, SUBTRACT, RESET) and updates the state accordingly.
  - **subscribe**: Accepts a function that gets called whenever the state changes. This function should log the new state to the console.
- **No UI Rendering**: This challenge focuses on state management without the complexity of UI rendering. All state changes should be observable through console logs.
- **Functional Programming Principles**: Draw upon functional programming concepts as illustrated in the reference videos. While Redux is the inspiration, you're encouraged to apply these principles creatively in your implementation.

## Submission Guidelines
Your submission should consist of a JavaScript file(s) that encapsulate your Redux-inspired store and the logic for dispatching actions and subscribing to changes. Include a README.md file explaining:
- How to run your code.
- A brief overview of your approach.
- Any challenges you faced and how you overcame them.

Ensure your code is well-commented and adheres to best practices for readability and maintainability.

## Evaluation Criteria
- **Correctness**: Your implementation should correctly handle the scenarios as outlined in the user stories.
- **Code Quality**: Use of functional programming principles, clear naming conventions, and code organization.
- **Documentation**: Clarity of your approach and reflections in the README.md.

This challenge is an excellent opportunity to demonstrate your understanding of state management concepts and functional programming principles. Good luck!

## Overview
This project demonstrates a simple, Redux-like state management system implemented in vanilla JavaScript. It simulates Redux's core concepts and uses an HTML file to open and interact with the JavaScript file in a web browser. The app implements a counter with actions to add, subtract, and reset, with each state change displayed in the browser console.

## How to Run
1. Open the `index.html` in a web browser.
2. Open the browser’s Developer Console.
3. Observe the console for log messages showing the initial state and each state change as actions are dispatched.

## Approach
The project demonstrates Redux-inspired state management by implementing the following:
- **Initial State**: A simple state with a count value of `0`.
- **Actions**: Three actions—`ADD`, `SUBTRACT`, and `RESET`—to adjust the count.
- **Reducer Function**: Updates the state based on the action dispatched, returning a new state.
- **Store Initialization**: A custom store with methods to:
  - `getState` retrieves the current state.
  - `dispatch` applies actions and updates the state.
  - `subscribe` registers listeners, logging changes to the console.

## Challenges
- The main challenge I faced was figuring out how to run the code and see the console output. 
- Initially, I completed the JavaScript logic but wasn't seeing results immediately. 
- I researched a few options, like running the file in Node.js or a browser console, but in the end, the simplest solution was to add a basic HTML file. Linking `store.js` in an HTML file made it easy to open the file in a web browser and check the console. 
- I found this approach straightforward and effective, as I could simply open `index.html` and view the output in the browser console without any additional setup.

- This solution helped me overcome the issue of accessing console logs easily and observing the state changes as I worked through each scenario.