# React III

## Router

* First install `react-router-dom`


* ```t
  import {
  BrowserRouter as Router,
  Switch,
  Route,
  Link
  } from "react-router-dom";
  ```

* A `<Switch>`looks through its children `<Route>` and enders the first one that matches the current URL.

## Styling and CSS

* Pass a string as the className prop
* CSS-in-JS” refers to a pattern where CSS is composed using JavaScript instead of defined in external files.
* React can be used to power animations. See:
    * React Transition Group
    * React Motion
    * React Spring

## Next.js

* Next.js has the best-in-class "Developer Experience" and many built-in features
* Next.js has two forms of pre-rendering: Static Generation and Server-side Rendering.
    * Static Generation is the pre-rendering method that generates the HTML at build time. The pre-rendered HTML is then reused on each request.
    * Server-side Rendering is the pre-rendering method that generates the HTML on each request.
* `npx create-next-app APP-NAME`
* `npm run dev`


[Main Page](https://will-ing.github.io/reading-notes)