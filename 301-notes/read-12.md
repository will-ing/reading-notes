# Components

## [EJS Partials](https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433)

>Partials come in handy when you want to reuse the same HTML across multiple views

*Be sure to make a folder for all your partials and name the `"the section".ejs`*

> This is a good to use to make your code more DRY. Think about using on Head, Header, Nav, Footer (etc..)

> `<%- %>` tags allow us to output the unescaped content onto the page. This is important when using the include() statement since you don’t want EJS to escape your HTML characters like ‘<’, ‘>’, etc…

```js
<%- include('partials/header') %>

<%- include('partials/navbar') %>

<%- include('partials/footer') %>
```




[Main Page](https://will-ing.github.io/reading-notes)