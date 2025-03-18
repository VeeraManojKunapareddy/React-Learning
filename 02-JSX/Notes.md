# What is JSX?

JSX is a syntax extension for JavaScript that allows you to write HTML-like code in your React components. It makes your code more readable and easier to write. For example:

```jsx
const element = <h1>Hello, JSX!</h1>;
```

This JSX code gets transformed into regular JavaScript using Babel:

```javascript
const element = React.createElement('h1', null, 'Hello, JSX!');
```

---

## How to Use JSX with React CDN and Babel

### Include Babel via CDN

To use JSX in your React CDN setup, you need to include Babel in your project. Add the following script tag to your HTML file:

```html
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
```

---

### Write JSX in Your Script

To tell the browser that your script contains JSX, you need to set the `type` attribute of your `<script>` tag to `text/babel`. This tells Babel to process the script before executing it.

Here’s an example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React with JSX</title>
</head>
<body>
    <div id="root"></div>

    <!-- React CDN Links -->
    <script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>

    <!-- Babel CDN -->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

    <script type="text/babel">
        // JSX code
        function App() {
            return (
                <div>
                    <h1>Hello, JSX!</h1>
                    <p>This is a React component using JSX.</p>
                </div>
            );
        }

        // Render the component into the DOM
        ReactDOM.render(<App />, document.getElementById('root'));
    </script>
</body>
</html>
```

The `type="text/babel"` attribute tells Babel to process the script.
