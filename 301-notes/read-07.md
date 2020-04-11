# API's continued

# [REST APIs](https://restfulapi.net/)

>REST stands for `REpresentational State Transfer`

REST has 6 guiding constraints

name | definition
----- | -----
Cient-server | By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.
Stateless | Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.
Cacheable | Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable.
Untiform interface | By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.
Layered system | The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting.
Code on Demand (Optional) | REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.
Resource

> `REST != HTTP`


# [SuperAgent](https://visionmedia.github.io/superagent/)


>SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs.

```js
 request
   .post('/api/pet')
   .send({ name: 'Manny', species: 'cat' })
   .set('X-API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(res => {
      alert('yay got ' + JSON.stringify(res.body));
   });
```

### Request basics

```js
request // request can be initiated by invoking the appropriate method on the request object,
   .get('/search')
   .then(res => { //then calling .then() (or .end() or await) to send the request.
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });
```

### Setting header fields

```js
// Setting header fields is simple, invoke .set() with a field name and value:

request
   .get('/search')
   .set('API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(callback);
```

### GET requests

```js

// .query() method accepts objects, which when used with the GET method will form a query-string. 

 request
   .get('/search')
   .query({ query: 'Manny' })
   .query({ range: '1..5' })
   .query({ order: 'desc' })
   .then(res => {

   });
```

[Main Page](https://will-ing.github.io/reading-notes)