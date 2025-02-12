# Reacting
In this chapter, you will learn about React's bread and butter: states!

## Before You Start
- Completion of [Chapter 2: Components](./2-components.md)
- A text editor

## What is a State?
Think of a state like a special variable that:
- Can change over time
- Automatically updates your website when it changes
- Remembers its value

## Creating Your First State
Let's update your project to include a counter that changes when clicked!

1. Open your `main.jsx` file
2. Replace everything with this new code:
    ```jsx
    import { StrictMode, useState } from 'react'
    import { createRoot } from 'react-dom/client'

    // Our Header component from before
    function Header({ text }) {
        return (
            <h1>{text}</h1>
        )
    }

    // Our App component with new state features!
    function App() {
        // This creates our state variable
        const [count, setCount] = useState(0);

        // This function runs when we click the button
        function incrementCount() {
            setCount(count + 1);
        }

        return (
            <div>
                <Header text="Hello," />
                <Header text="World!" />
                <Header text={`Times clicked: ${count}`} />
                <button onClick={incrementCount}>Count</button>
            </div>
        )
    }

    createRoot(document.getElementById('root')).render(
        <StrictMode>
            <App />
        </StrictMode>
    )
    ```

## What's New?

### 1. Importing useState
```jsx
import { StrictMode, useState } from 'react'
```
- `useState` is React's special tool for creating states
- We need to import it before we can use it

### 2. Creating a State
```jsx
const [count, setCount] = useState(0);
```
This line creates a state with:
- `count`: the variable that holds our number
- `setCount`: a function to update our number
- `useState(0)`: starts the count at 0

### 3. Creating an Update Function
```jsx
function incrementCount() {
    setCount(count + 1);
}
```
This function:
- Takes the current `count`
- Adds 1 to it
- Uses `setCount` to update the state

### 4. Using the State
```jsx
<Header text={`Times clicked: ${count}`} />
<button onClick={incrementCount}>Count</button>
```
- We display the current count in a Header
- We create a button that runs `incrementCount` when clicked

## See It in Action!
1. Start your project:
   ```
   npx vite
   ```
2. Open your browser to the shown address
3. Click the "Count" button
4. Watch the number increase each time!

## Challenges
Try these challenges:
1. Add a "Reset" button that sets count back to 0
2. Create a "Decrease" button that subtracts 1
3. Change the starting number

## Common Questions

### Why use states?
- They automatically update your webpage
- They remember values between renders
- They're perfect for interactive elements

### When should I use a state?
Use a state when you have:
- Values that change over time
- User input to track
- Data that needs to update the display

### Why not just use a regular variable?
Regular variables:
- Don't trigger page updates
- Reset when React re-renders
- Don't preserve their values

## What's Next?
[Chapter 4: Real-World React](./4-real-world-react.md)