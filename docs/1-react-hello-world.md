# React: Hello, World!

This chapter guides you through creating a React project from scratch. By the end, you'll have a webpage that displays "Hello, World!" using React.

## What You'll Need
- A computer with Node.js installed
- A text editor
- Basic knowledge of using the terminal/command prompt

## Step 1: Setting Up Your Project Folder
1. Open your computer's file explorer
2. Create a new folder called `react-hello-world` wherever you'd like

## Step 2: Preparing Your Project
1. Open your terminal/command prompt
2. Navigate to your `react-hello-world` folder
   ```
   cd C:\path\to\react-hello-world
   ```
3. Run this command to create a new project:
   ```
   npm init -y
   ```
   This creates a special file called `package.json` that helps manage your project.

4. Now install React and its tools by running:
   ```
   npm install react react-dom vite @vitejs/plugin-react
   ```

## Step 3: Creating Your Project Files
You'll need to create three important files. Let's make them one at a time:

### File 1: Vite Configuration
1. Create a new file called `vite.config.js`
2. Copy and paste this code into it:
   ```js
   import { defineConfig } from 'vite'
   import react from '@vitejs/plugin-react'

   export default defineConfig({
       plugins: [react()],
   })
   ```
   This tells Vite (a development tool) to use React.

### File 2: React Code
1. Create a new file called `main.jsx`
2. Copy and paste this code into it:
   ```jsx
   import { StrictMode } from 'react'
   import { createRoot } from 'react-dom/client'

   createRoot(document.getElementById('root')).render(
       <StrictMode>
           <h1>Hello, World!</h1>
       </StrictMode>
   )
   ```
   This is your actual React code that will show "Hello, World!"

### File 3: HTML Page
1. Create a new file called `index.html`
2. Copy and paste this code into it:
   ```html
   <!doctype html>
   <html lang="en">
       <head>
           <meta charset="UTF-8" />
           <meta name="viewport" content="width=device-width, initial-scale=1.0" />
           <title>My First React App</title>
       </head>
       <body>
           <div id="root"></div>
           <script type="module" src="/main.jsx"></script>
       </body>
   </html>
   ```
   This is the webpage that will display your React content.

## Step 4: Running Your Project
1. In your terminal (make sure you're still in the `react-hello-world` folder), run:
   ```
   npx vite
   ```
2. You should see a message with a website address (usually `http://localhost:5173` or similar)
3. Open your web browser and go to that address
4. You should see "Hello, World!" displayed on the page

You've just created a React project!

## What's Next?
[Chapter 2: Components](./2-components.md)