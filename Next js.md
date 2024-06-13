Next JS @13.3.4 Step by step guide
================================================================
***
## Day-00
#23. Test Sample Notes Data
--------------------------------------------------------
### Use Cases:
* **Lifecycle Management**: React manages the mounting, updating, and unmounting of the component. This allows for the use of hooks and lifecycle methods.
* **State and Props**: The component can manage its own state and receive props, making it more flexible and reusable.
* **Hooks Support**: If `InnerComp` uses hooks like `useState` or `useEffect`, these hooks will function as expected within the component lifecycle.
* **Ref and Context Handling**: It can properly handle React refs and contexts.
* **Context**: The component
* Style with next.js 13.4(Inline styling,global css)
* #22 CSS Modules with Next.js 13.4
* 1st text.
* **2nd text**: with bold
In our main `Home` component, we can render `InnerComp` in two ways:
1.  **As a React component**: `<InnerComp />`
2.  **As a function call**: `{InnerComp()}`

Consider a simple React component called `InnerComp` that renders a message:
```jsx
const InnerComp = () => {
  return <h1>Hello from InnerComp</h1>;
};
```


***
## Day: 03
#21. Style with Next.JS(Inline styling,global css)
------------------------------------------------------------
### Use Cases:
*   **Inline Styling**: in Next.JS the inline styling are as same as Reach like `style={{}}`.
*   **Global CSS**: The global css are used to define styling globally in an project for ex: button color.
*   **Priority**: If we use inline css for the same class written in global css file the priority will be given to the inline css.

#22. CSS Modules
------------------------------------------------------------
### Use Cases:
* **CSS Modules** are used for duplicate class declaration purpose in Next.JS
* lets say we have a default button i.e **global** component and we want to override it,then we can simply create it using **CSS modules**.
* we create the css module in `<name>.module.css` format and import it like `import <name> from '<name>.module.css;`
* **Use's**: fo button CSS simply use by `<importname>.button` in the code.
* Uses:
```css
.firstcustom {
    color: aquamarine;
    background-color: black;
}
```
```jsx
"use client"
import React from 'react'
import outside from '../../styles/outside.module.css'

const PageButton = () => {
    return (
        // <button onClick={() => alert('Hola')} style={[outside.button,{ borderRadius: "15px", backgroundColor: "#2654fd" }]}>Clic to show price</button>
        <button onClick={() => alert('Hola')} className={outside.firstcustom}>Clic to show price</button>
    )
}

export default PageButton
```


