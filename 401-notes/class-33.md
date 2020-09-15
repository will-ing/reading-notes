# Authentication & Production Server

## Web Tokens

> JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

You should use Web tokens for `Authorization` and `information exchange`.

### Structure of a web Token

* Payload
* Header
* Signature

### define

* The `header` typically consists of two parts
* The second part of the token is the `payload`, which contains the claims. Claims are statements about an entity
  * Registered claims
  * Public claims
  * Pivate claims

-----

## JWT

>The JWT is just an authorization token that should be included in all requests:

* The access token is usually short-lived
* The refresh token lives a little bit longer

Install:

1. ```t
    poetry add djangorestframework_simplejwt
    ```

2. ```py
   from rest_framework_simplejwt import views as jwt_views
   ```

[Main Page](https://will-ing.github.io/reading-notes)