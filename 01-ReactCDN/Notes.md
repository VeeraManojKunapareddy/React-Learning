# What is React?

React is a JavaScript library for building user interfaces (UIs). It’s used to create dynamic, interactive, and reusable components for web applications. For example, if you’re building a website with buttons, forms, or dynamic content that updates without refreshing the page, React can help you do that efficiently.

React was created by Facebook and is now widely used by developers worldwide.

---

## What is a CDN?

CDN stands for **Content Delivery Network**. It’s a system of servers distributed around the world that deliver files (like JavaScript, CSS, or images) to users based on their geographic location. Using a CDN makes loading files faster because the files are served from a server closer to the user.

---

## What is React CDN?

When you’re learning React or building a small project, you don’t always need to set up a complex development environment. Instead, you can use React directly in your HTML file by including it via a **CDN link**. This means you’re pulling the React library from a CDN server instead of downloading and hosting it yourself.

### React CDN Files:

- **react.development.js**: This is the core React library.
- **react-dom.development.js**: This is the library that allows React to interact with the DOM (Document Object Model).

### Essential React Methods:

- **React.createElement()**: This is how you create elements in React.
- **ReactDOM.render()**: This renders your React component into the DOM.

---

## What is CORS?

CORS stands for **Cross-Origin Resource Sharing**. It’s a security feature implemented by web browsers to control how resources are requested from another domain outside the domain from which the resource originated. This is important for preventing malicious websites from accessing sensitive data on another site.

### How CORS Works:

When a web application makes a request to a different domain (cross-origin request), the browser sends an HTTP request with an `Origin` header. The server can then respond with specific headers (`Access-Control-Allow-Origin`, `Access-Control-Allow-Methods`, etc.) to indicate whether the request is allowed.

### Common CORS Headers:

- **Access-Control-Allow-Origin**: Specifies which origins are allowed to access the resource.
- **Access-Control-Allow-Methods**: Specifies the methods (GET, POST, etc.) allowed when accessing the resource.
- **Access-Control-Allow-Headers**: Specifies which headers can be used in the actual request.

### Using `crossorigin` in Script Tags

When including scripts from a CDN or other external sources in your React project, you might need to use the `crossorigin` attribute in your `<script>` tags. This attribute is used to handle cross-origin requests and can be important for security and proper functioning of your application.

#### Example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React CDN Example</title>
</head>
<body>
    <div id="root"></div>
    <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
    <script>
        const element = React.createElement('h1', null, 'Hello, world!');
        ReactDOM.render(element, document.getElementById('root'));
    </script>
</body>
</html>
```

#### Values for `crossorigin`:

- **anonymous**: This is the default value. It sends a request without credentials (cookies, client-side SSL certificates, or HTTP authentication).
- **use-credentials**: This sends a request with credentials.
