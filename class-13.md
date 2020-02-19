# Local storage

[THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS](http://diveinto.html5doctor.com/storage.html)

### Downside of cookies

1. They're included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
2. They're included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
3. They're limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful

>HTML5 storage -  it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. 

type | description
---- | ----
setItem() | with a named key that already exists will silently overwrite the previous value.
removeItem()| methods for removing the value for a given named key
key() | 

### TRACKING CHANGES TO THE HTML5 STORAGE AREA

>You can trap the storage event. The storage event is fired on the window object whenever `setItem(), removeItem(), or clear() `is called and actually changes something.

```js
if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};
```
The handle_storage callback function will be called with a StorageEvent object, except in Internet Explorer where the event object is stored in window.event.

```js
function handle_storage(e) {
  if (!e) { e = window.event; }
}

```
At this point, the variable e will be a StorageEvent object, which has the following useful properties.

### limitation of todays storage systems

1. `5 megabytes` -is how much storage space each origin gets by default.
2. `QUOTA_EXCEEDED_ERR` -is the exception that will get thrown if you exceed your storage quota of 5 megabytes.
3. `no` -  is the answer to the next obvious question, “Can I ask the user for more storage space?

>Data is stored as a string.




[Main Page](https://will-ing.github.io/reading-notes)