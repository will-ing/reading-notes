# EJS

## What is EJS?

`EJS` is a simple templating language that lets you generate HTML markup with plain JavaScript.

Install
It's easy to install EJS with NPM.

```
$ npm install ejs
```

Use
Pass EJS a template string and some data. BOOM, you've got some HTML.

```js
let ejs = require('ejs'),
    people = ['geddy', 'neil', 'alex'],
    html = ejs.render('<%= people.join(", "); %>', {people: people});
```

Browser support
Download a browser build from the latest release, and use it in a script tag.

```js
<script src="ejs.js"></script>
<script>
  let people = ['geddy', 'neil', 'alex'],
      html = ejs.render('<%= people.join(", "); %>', {people: people});
</script>
```

- <% Scriptlet tag, for control-flow, no output\
- <%_ ‘Whitespace Slurping’ Scriptlet tag, strips all whitespace before it\
- <%= Outputs the value into the template (HTML escaped)\
- <%- Outputs the unescaped value into the template\
- <%# Comment tag, no execution, no output\
- <%% Outputs a literal <%\
- %> Plain ending tag\
- -%> Trim-mode ('newline slurp') tag, trims following newline
- _%> ‘Whitespace Slurping’ ending tag, removes all whitespace after it

[Main Page](https://will-ing.github.io/reading-notes)