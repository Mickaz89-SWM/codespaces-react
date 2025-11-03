---
title: React
---
# Introduction

This document explains the setup and initialization of the React application in <SwmPath>[src/index.jsx](/src/index.jsx)</SwmPath>. It covers:

1. How the React root is created and the app is rendered.
2. Why <SwmToken path="/src/index.jsx" pos="9:2:4" line-data="  &lt;React.StrictMode&gt;">`React.StrictMode`</SwmToken> is used around the app.
3. How performance measurement is integrated and why environment logging is included.

# creating the React root and rendering the app

<SwmSnippet path="/src/index.jsx" line="1">

---

The entry point uses <SwmToken path="/src/index.jsx" pos="7:6:8" line-data="const root = ReactDOM.createRoot(document.getElementById(&#39;root&#39;));">`ReactDOM.createRoot`</SwmToken> to create a root container attached to the DOM element with id <SwmToken path="/src/index.jsx" pos="7:2:2" line-data="const root = ReactDOM.createRoot(document.getElementById(&#39;root&#39;));">`root`</SwmToken>. This is the modern React 18+ API for concurrent rendering. The root then renders the <SwmToken path="/src/index.jsx" pos="10:1:4" line-data="    &lt;App /&gt;">`<App />`</SwmToken> component wrapped in <SwmToken path="/src/index.jsx" pos="9:1:5" line-data="  &lt;React.StrictMode&gt;">`<React.StrictMode>`</SwmToken>. This setup ensures the app is mounted properly and benefits from React's strict mode checks during development.

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

# using <SwmToken path="/src/index.jsx" pos="9:2:4" line-data="  &lt;React.StrictMode&gt;">`React.StrictMode`</SwmToken>

Wrapping <SwmToken path="/src/index.jsx" pos="10:1:4" line-data="    &lt;App /&gt;">`<App />`</SwmToken> in <SwmToken path="/src/index.jsx" pos="9:1:5" line-data="  &lt;React.StrictMode&gt;">`<React.StrictMode>`</SwmToken> enables additional checks and warnings for potential problems in the app. It helps catch unsafe lifecycles, deprecated APIs, and other side effects early. This wrapper does not affect production behavior but improves code quality during development.

# performance measurement and environment logging

The code calls <SwmToken path="/src/index.jsx" pos="19:0:2" line-data="reportWebVitals();">`reportWebVitals()`</SwmToken> to enable performance metrics collection. This function can be configured to log or send metrics to analytics endpoints, helping track app performance over time.

<SwmSnippet path="/src/index.jsx" line="14">

---

Additionally, the code logs a simple message confirming the app is running and outputs the current environment (`development`, `production`, etc.) from <SwmToken path="/src/index.jsx" pos="18:10:14" line-data="console.log(&#39;Environment:&#39;, process.env.NODE_ENV);">`process.env.NODE_ENV`</SwmToken>. This helps verify the build context during startup.

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
