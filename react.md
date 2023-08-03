# react.dev

React is a JS library for building dynamic & interactive user interfaces.

Component-based
Declarative
State-driven

Prerequisites: HTML CSS JS ; Plus: TS
JS imp concepts: ES6 modules, array/object destructuring, array methods (map filter reduce ..), promises, ternary operator(?:), arrow functions(=>), short circuiting(&&),

Working with plain/vanilla JS DOM becomes complex as application grows.
Here React helps, with it we describe the webpage using small reusable components and React takes care of efficiently creating and updating DOM elements.

Components help us write reusable, modular, and better organized code.
eg. in a movie streaming app the components can be: Navbar TrendingCarousel FilterMenu MoviesGrid

## Ways to create a React app

### Old way (full setup from base)

1. Install node.js
2. New folder for project & open in terminal
3. Initialize a new npm project > npm init -y
4. Install necessary dependencies for your react project.
    - Two package needed > npm install react react-dom
5. Install Babel(a tool that therepiles ES6+ code to ES5 for older browsers)
    - npm install --save dw @babel/core @babel/preset-env @babel/preset-react ...
6. Create a new file .babelrc and add {"presets":["@babel/preset-env", "@bab.."]}
7. Create a file 'webpack.config.js' and add the following code: [code not written here but its webpack config code]
8. Create a new directory 'src' -> index.html, index.js,
9. Run this to build react app > npx webpack .

### New way

#### create-react-app (CRA)

```sh
    > npx create-react-app app-name
    ...
    > npm start
```

#### Vite [newer beter way]

```sh
    > npm create vite@latest  /  npm init vite 
    # Project name : .  (. for the same folder you are in / any name for creating app inside the folder)
    # OR 
    > npm create vite@latest my-app-name

    Select a framework: React
    Select a variant: JS/TS

    > cd my-app-name    (if not inside the app folder; '.' puts in same folder)
    > code .    (if not inside vscode)

    > npm install  /  npm i 
    > npm run dev
```

## Project Structure

- node_modules - folder with 3rd party libraries (npm packages)
- public - folder for public assets
- src - source code of application
        - App.css - app component styles
        - App.tsx - app component
        - index.css - main component styles
        - main.tsx - main component
        - vite-env.d.ts - x
- .gitignore - x
- index.html - x
- package-lock.json - x
- package.json - x
- tsconfig.json - x
- tsconfig.node.json - x
- vite.config.ts - x

.js / .ts - for plain js/ts files
.jsx / .tsx - for react components

Two ways to create a react component
    JS Class -
    JS Function - new & popular cause easier to write; hooks used for

Component:
It is basically a part of your application.
A function inside React starting with a capital letter is simply just a component.
Components name must be in PascalCase.
A component always returns a JSX element.
The whole JSX should be inside a single parent element like `<div></div>` or a fragment `<></>` because it only returns one element.

JSX: JavaScript XML
babeljs.io/repl - site to check conversion of jsx-html to js
With JSX we can describe UI of our app, create dynamic content using JS inside html
Some differences: class - className , for - htmlFor ,
To run JavaScript inside JSX use {}
To start JSX inside JavaScript use any html <element/tag></>

Each child in a list should have a unique "key" prop.
If you return an array of elements inside of react, make sure each element at the top level has a "key" property eg. `<li key={todo.id}>...</li>`
This id must be any unique id; And dont use the index of the array because it can mess up with change.

Component tree - tree of parent child components
When app starts React takes the component tree and builds VirtualDOM(a JS dataStr); its different from the realDOM in browser; its lightweight in-memory representation of component tree, where each node represent a component and its properties.
When data of a component changes React updates the corresponding node in the VirtualDOM to reflect the new state, then it compares it with the previous version of VirtualDOM to identify the nodes to update.
Updating the DOM is done by its companion library ReactDOM.

## React dev process

Building components
Rendering markup with JSX
Managing state (simply variable / data managed by component)
Passing input via props (props - inputs passed to components; this make the component reusable)
Debugging React apps

## Learning process

JSX Components States Props
CSS - inline, .css files, css frameworks, styled components(library)
conditional rendering
iterational rendering
import external data
Routing (connect multiple pages)
Redux
context API
Fetch APIs (fetch, axios)
Component life cycle
Hooks
Testing
Server side rendering

Use css libraries with React:
> npm i bootstrap@5.2.3     (version @5.2.3 is optional need)
In any component file: import 'bootstrap/dist/css/bootstrap.css'

React Declarative approach:
I want my site to look like this - wrote JSX how to look like
Now adding interactivity - instead of saying manually to change the value - we change the JSX and say i want this value to be this specific variable and so on
Just declaring how the output would be like - and react does the magic behind the scene.

Naming conventions:
    variable setVariable
    onClick handleClick
on - thats an event;  syntax: `on${EventName}`  eg. onClick onChange onInput ...
handle - used for function name to handle certain event

// Hooks -
Hooks need to be called in the top level of the function ie. direct inside the function or component not inside any other block.

useState - change state of a value (simply modify variables)

    To modify variables and have things interactive we need 'state'
    useState() - this is a hook inside react which we can import and use.
    useState essentialy takes a default value, it can be any value stringnull or even a function.
    It returns us an array of two things:
        1st variable with the value of our thing
        2nd a function for updating our value
    eg. const [newItem, setNewItem] = useState('');
        newItem will have the value (here '' empty string as provided)
        setNewItem is the function to update the newItem value
    {this is a naming convention as like variable and setVariable}

    Here, you cannot update a state variable (ie. newItem here) because its immutable
    Instead call the function (ie. setNewItem here) with the new value as an argument
    eg. setNewItem('This is new value');

    When you change a state variable (eg. through setVariable) it always re-renders your entire component. So, it updates everywhere thats used inside the component.

    Normally, setState will 'change' the data on passing a value.
    But to 'modify' the existing data of the variable (if you need the current data) - pass a function to setState (ie. setVariable here) instead of just value.
    This function takes the current value of the state as an argument & returns 

useEffect -
    this hook doesnt return anything but takes a function & a second property as its argument; it run the function everytime the object in the second property change.

// Props - inputs to components to make it reusable ie. change data in same component
props let you pass information to custom components
