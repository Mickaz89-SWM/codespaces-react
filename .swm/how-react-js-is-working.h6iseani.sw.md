---
title: How React Js is working
---
<SwmSnippet path="/src/index.jsx" line="1">

---

&nbsp;

```javascript
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

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals(); //hello
```

---

</SwmSnippet>

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBY29kZXNwYWNlcy1yZWFjdCUzQSUzQU1pY2thejg5LVNXTQ==" repo-name="codespaces-react"><sup>Powered by [Swimm](https://staging.swimm.cloud/)</sup></SwmMeta>
