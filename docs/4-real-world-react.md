# Real-World React Projects
Congratulations on learning the basics of React! Now let's see how a React project would be set up in a real-world scenario.

## Why Change Our Approach?
In previous chapters, we built everything from scratch to understand how React works.

We will be using a project generator - a tool that sets up everything we need in seconds - to create a new React project using industry-standard best practices.

## Creating a Professional React Project

### Step 1: Using the Vite Project Generator
1. Open your terminal
2. Navigate to where you want to create your project
3. Run this command:
   ```bash
   npm create vite@latest
   ```

### Step 2: Project Setup Wizard
You will see a setup wizard. Here's how to use it:

1. **Project Name**
   - Press Enter to accept `vite-project` or type a different name
   - This will be your project folder name

2. **Framework Selection**
   - Use the arrow keys (↑↓) to select `React`
   - Press Enter to select it
   
3. **Variant Selection**
   - Use the arrow keys to select `JavaScript`
   - Press Enter to choose it

4. **Final Setup**
   ```bash
   cd vite-project    # Go into your new project folder
   npm install        # Install all needed packages
   npm run dev        # Start your development server
   ```

5. Open your browser to the shown address (usually `http://localhost:5173`)

In just a few seconds, you now have a professional React setup!

## Project Structure

Your new project has a structure like this:
```
vite-project/
├── node_modules/    (All project dependencies)
├── public/          (Static files like images)
├── src/             (Your source code)
│   ├── App.jsx      (Main component)
│   ├── App.css      (Main component's stylesheet)
│   ├── main.jsx     (Entry point)
│   └── index.css    (Your main stylesheet)
├── index.html       (Main HTML file)
└── package.json     (Project configuration)
```

## Best Practices

### 1. Component Organization
Instead of putting all components in one file, create separate files.

For example, in previous chapters we had the following in the same file, but these would be placed in separate files.

```jsx
// src/components/Header.jsx
export function Header({ title }) {
    return <h1>{title}</h1>
}

// src/components/Button.jsx
export function Button({ onClick, children }) {
    return <button onClick={onClick}>{children}</button>
}

// src/App.jsx
import { Header } from './components/Header'
import { Button } from './components/Button'
```

### 2. File Naming Conventions
- Use PascalCase for component files: `Header.jsx`, `Button.jsx`
- Use camelCase for all other files: `helpers.js`, `utils.js`

### 3. Quality of Life Tools
Consider using these popular tools:
- **Styling**: Tailwind CSS or styled-components
- **Routing**: React Router for multiple pages

### 4. For Bigger Projects
Consider these frameworks:
- **Next.js**: For full-stack React applications
- **Remix**: For modern web applications
- **Gatsby**: For static websites