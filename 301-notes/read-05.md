# Heroku Deployment

### [node.js for beginners](https://howtonode.org/deploy-blog-to-heroku)


[Heroku getting started](https://devcenter.heroku.com/articles/getting-started-with-nodejs)


>node.js - is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications.

1. Create a JS file!
```js
var http = require("http");


http.createServer(function(request, response) {
  response.writeHead(200, {"Content-Type": "text/plain"});
  response.write("It's alive!");
  response.end();
}).listen(3000);

```

2. run `node server.js` or `npm start`\
  Your new server's address is http://localhost:3000/\
  check your ip address.


## [Demo Code from lecture](https://github.com/codefellows/seattle-301n17/blob/master/class-05/demo/city-explorer-lite/app.js)
```js
'use strict';

function setupEventListeners() {
  $('#search-form').on('submit', fetchCityData);
}

function fetchCityData(event) {
  event.preventDefault();
  let searchQuery = $('#input-search').val().toLowerCase();
  getLocation(searchQuery);
}

function getLocation() {

  $.ajax('/fake-data/location.json')
    .then( location => {
      showTitle(location);
      showMap(location);
      getRestaurants(location);
    });

}

function showTitle(location) {
  // container = #title
  // template = #title-template
  // data == location

  let $template = $('#title-template').html();
  let $target = $('#title');
  let html = Mustache.render( $template, location );
  $target.html(html);

}

function showMap(location) {
  // container = #title
  // template = #title-template
  // data == location

  let $template = $('#map-template').html();
  let $target = $('#map');
  let html = Mustache.render($template, location);
  $target.html(html);
}

function getRestaurants(location) {
  // container = #restaurants-results
  // template = #restaurants-results-template
  // data == come from an ajax call

  let $template = $('#restaurants-results-template').html();
  let $target = $('#restaurants-results');

  $.ajax('/fake-data/restaurants.json')
    .then( list => {
      list.forEach( restaurant => {
        let html = Mustache.render($template, restaurant);
        $target.append(html);
      });
    });

}

$(document).ready(function() {
  setupEventListeners();
});
```

The HTML

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <title>Document</title>
  <link rel="stylesheet" href="style.css" />

  <script id="map-template" type="x-tmpl-mustache">
    <img src="/images/map.png?lat={{latitude}}&lng={{longitude}}" height="300" width="400" />
  </script>

  <script id="title-template" type="x-tmpl-mustache">
    <span>Here are the results for {{formatted_query}}</span>
  </script>

  <script id="restaurants-results-template" type="x-tmpl-mustache">
    <li>
      <div>{{restaurant}}</div>
      <div>{{cuisines}}</div>
      <div>{{locality}}</div>
    </li>
  </script>

</head>

<body>

  <header>
    <h1>City Explorer</h1>
    <p>Enter a location below to learn more about it</p>
  </header>

  <main>
    <form id="search-form">
      <label>
        <span>Search for a location</span>
        <input name="search" id="input-search" placeholder="Enter a city name" />
        <button type="submit">Explore!</button>
      </label>
    </form>

    <section id="map"></section>

    <h2 id="title"></h2>

    <section class="columns">
      <section id="restaurants">
        <h3>Restaurants</h3>
        <ul id="restaurants-results"></ul>
      </section>
    </section>

  </main>

  <script src="https://code.jquery.com/jquery-3.4.1.js"></script>
  <script src="https://unpkg.com/mustache@latest"></script>
  <script src="app.js"></script>
</body>

</html>

```