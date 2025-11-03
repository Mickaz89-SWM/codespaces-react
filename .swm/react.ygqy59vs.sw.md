---
title: React
---
# Introduction

This document explains the setup and initialization of the React application in <SwmPath>[src/index.jsx](/src/index.jsx)</SwmPath>.

We will cover:

1. How the React root is created and the app is rendered.
2. Why <SwmToken path="/src/index.jsx" pos="9:2:4" line-data="  &lt;React.StrictMode&gt;">`React.StrictMode`</SwmToken> is used.
3. How performance measurement is integrated and environment info is logged.

# creating the React root and rendering the app

The entry point uses <SwmToken path="/src/index.jsx" pos="7:6:8" line-data="const root = ReactDOM.createRoot(document.getElementById(&#39;root&#39;));">`ReactDOM.createRoot`</SwmToken> to create a root container attached to the DOM element with id <SwmToken path="/src/index.jsx" pos="7:2:2" line-data="const root = ReactDOM.createRoot(document.getElementById(&#39;root&#39;));">`root`</SwmToken>. This is the modern React 18+ API for concurrent rendering. The root then renders the <SwmToken path="/src/index.jsx" pos="10:1:4" line-data="    &lt;App /&gt;">`<App />`</SwmToken> component wrapped in <SwmToken path="/src/index.jsx" pos="9:1:5" line-data="  &lt;React.StrictMode&gt;">`<React.StrictMode>`</SwmToken>. This setup ensures the entire React component tree starts from <SwmToken path="/src/index.jsx" pos="4:2:2" line-data="import App from &#39;./App&#39;;">`App`</SwmToken> and is managed by React's rendering engine.

<SwmSnippet path="/src/index.jsx" line="1">

---

Using <SwmToken path="/src/index.jsx" pos="9:2:4" line-data="  &lt;React.StrictMode&gt;">`React.StrictMode`</SwmToken> enables additional checks and warnings during development without affecting production behavior. It helps catch potential issues early by intentionally invoking certain lifecycle methods twice and highlighting deprecated APIs.

```
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

---

</SwmSnippet>

# logging environment and measuring performance

After rendering, the code logs a simple message confirming the app is running and outputs the current environment (`development`, `production`, etc.) from <SwmToken path="/src/index.jsx" pos="18:10:14" line-data="console.log(&#39;Environment:&#39;, process.env.NODE_ENV);">`process.env.NODE_ENV`</SwmToken>. This helps verify the build context at runtime.

<SwmSnippet path="/src/index.jsx" line="14">

---

The <SwmToken path="/src/index.jsx" pos="15:14:14" line-data="// to log results (for example: reportWebVitals(console.log))">`reportWebVitals`</SwmToken> function is called without arguments here, but it can be configured to measure and report app performance metrics like load time or responsiveness. This is useful for monitoring and optimizing the app but is optional.

```
// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
console.log('App is running');
console.log('Environment:', process.env.NODE_ENV);
reportWebVitals();
```

---

</SwmSnippet>

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBY29kZXNwYWNlcy1yZWFjdCUzQSUzQU1pY2thejg5LVNXTQ==" repo-name="codespaces-react"><sup>Powered by [Swimm](http://localhost:5000/)</sup></SwmMeta>
