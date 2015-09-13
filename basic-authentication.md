# Service: basic-authentication

basic authentication utils for web apps

Note: this service is not a middleware, check **authentication** service for middlewares

## Interface

`````javascript
var basicAuth = imports['basic-authentication'];
`````

#### basicAuth.isValid([String] username, [function] done)
Check if the user is valid or not.

done(error, [String] permission)

permission could be one of the following:
- read
- *
- null

#### basicAuth.authenticate([String] username, [String] password, [function] done)
Authenticate by username and password

done(error, [String] permission)

permission could be one of the following:
- read
- *
- null

#### basicAuth.enabled()
check if the basic auth is enabled

#### basicAuth.defaultPermission()
get the default permission, return a string, could be one of the following:

- read
- *
