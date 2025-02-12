# React Components
In this chapter you will learn about Components, the building blocks that make React so powerful.

## Before You Start
Make sure you have:
- Completed the [previous chapter](./1-react-hello-world.md)
- Your `react-hello-world` project folder open

## What are Components?
Think of components like LEGO blocks for websites:
- You can use them multiple times
- You can pass different information to them
- They help keep your code organized

## Step 1: Creating Your First Components
Let's update your project to use components!

1. Find and open your `main.jsx` file in the `react-hello-world` folder
2. Replace everything in it with this new code:
    ```jsx
    import { StrictMode } from 'react'
    import { createRoot } from 'react-dom/client'

    // This is our first component
    // It's a special header that can display any text we give it
    function Header({ text }) {
        return (
            <h1>{text}</h1>
        )
    }

    // This is our main App component
    // It uses our Header component twice
    function App() {
        return (
            <div>
                <Header text="Hello," />
                <Header text="World!" />
            </div>
        )
    }

    // This connects our App to the webpage
    createRoot(document.getElementById('root')).render(
        <StrictMode>
            <App/>
        </StrictMode>
    )
    ```

### What's New?:

1. **The Header Component**
   ```jsx
   function Header({ text }) {
       return (
           <h1>{text}</h1>
       )
   }
   ```
   - This is a reusable component that creates a heading (``<h1>``)
   - `{ text }` means it accepts a piece of text to display
   - You can use it multiple times with different text
   - Don't get confused by the two pairs of curly brackets!
     - The first, ``{ text }`` tells the component to expect a value to be given to it.
     - The second, ``{text}`` tells React to place that value in the component.
     - If you replaced the second one with ``text``, your component could only ever have the text "text". Similar to how we displayed "Hello, World!" in the previous chapter.

2. **The App Component**
   ```jsx
   function App() {
       return (
           <div>
               <Header text="Hello," />
               <Header text="World!" />
           </div>
       )
   }
   ```
   - This is your main component that organizes everything
   - It uses the `Header` component twice
   - Each `Header` gets different text to display

## Step 2: See It in Action!
1. Open your terminal
2. Make sure you're in the `react-hello-world` folder
3. Run this command:
   ```
   npx vite
   ```
4. Open your web browser to the address shown (usually `http://localhost:5173`)
5. You should see:
   ```
   Hello,
   World!
   ```
   Each line is created by a separate `Header` component!

## Common Questions
### What's with the curly braces?
  - `{ text }` in the component definition lets you receive information
  - `{text}` in the HTML lets you use JavaScript variables in your display

## What's Next?
[Chapter 3: Reacting](./3-reacting.md)