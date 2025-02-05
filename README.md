# useParams Hook Error in Conditionally Rendered Component

This repository demonstrates an uncommon error in React Router v6 when using the `useParams` hook within a conditionally rendered component.  The issue arises when the component renders before the necessary data for determining the route parameters is available, causing `useParams` to return `undefined`. Accessing properties of this `undefined` value then leads to runtime errors.

## How to reproduce

1. Clone this repository.
2. Navigate to the `bug.js` file to see the code causing the problem.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Navigate to a route that triggers the conditional rendering and data fetching.
6. Observe the error in your browser's console.

## Solution

The solution, shown in `bugSolution.js`, involves carefully checking if `useParams` returns `undefined` before attempting to access its properties.  This can be done using optional chaining or other null-safe techniques.