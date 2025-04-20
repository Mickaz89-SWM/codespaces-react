---
title: How React Js is working ?
---
# Introduction

This document will walk you through the main components of how React JS is set up in our project. The purpose is to understand the initial setup and performance measurement integration.

We will cover:

1. How the application is rendered using React.
2. How performance metrics are integrated.

# Application rendering

<SwmSnippet path="/src/index.jsx" line="1">

---

The application is rendered using React's <SwmToken path="/src/index.jsx" pos="7:6:8" line-data="const root = ReactDOM.createRoot(document.getElementById(&#39;root&#39;));">`ReactDOM.createRoot`</SwmToken> method. This is a crucial step as it initializes the root of the React component tree and attaches it to the DOM element with the id 'root'. The <SwmToken path="/src/index.jsx" pos="4:2:2" line-data="import App from &#39;./App&#39;;">`App`</SwmToken> component is wrapped in <SwmToken path="/src/index.jsx" pos="9:2:4" line-data="  &lt;React.StrictMode&gt;">`React.StrictMode`</SwmToken>, which helps identify potential problems in the application by enabling additional checks and warnings.

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

# Performance measurement

<SwmSnippet path="/src/index.jsx" line="14">

---

Performance metrics are integrated using the <SwmToken path="/src/index.jsx" pos="15:14:14" line-data="// to log results (for example: reportWebVitals(console.log))">`reportWebVitals`</SwmToken> function. This function allows us to measure and log performance results or send them to an analytics endpoint. This is important for monitoring and optimizing the application's performance over time.

```
// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```

---

</SwmSnippet>

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBY29kZXNwYWNlcy1yZWFjdCUzQSUzQU1pY2thejg5LVNXTQ==" repo-name="codespaces-react"><sup>Powered by [Swimm](http://localhost:5000/)</sup></SwmMeta>
