# Service: middlewares

## Description
Common express middlewares.

## Interface

You need to consume **middlewares** service in your plugin, and get middlewares instance with following code:
`````javascript
var middlewares = imports.middlewares;
`````

### middlewares.all([Optional, Array(String)] list)
get a list of instances of registered middlewares. Or get the instances of middlewares specified in the list.

By default, the list of middlewares are:
`````javascript
[
    'morgan',
    'cookieParser',
    'urlEncodedParser',
    'jsonParser',
    'session'
];
`````


### middlewares.register([String] name, [function] middleware, [optional, int] index)
Register a middleware named **name** at the index**th** position of the middleware list. If index parameter is not found, the middleware is appended at the end of the list

For example, we could register a new **test** middleware after **jsonParser** by following code:

`````javascript
middlewares.register('test', function(req, res, next){
    // your middlewere code here
    next();
}, 4);
`````

### middlewares.remove([String] name)
Remove a middleware from list

## Implementation

### Plugin: fx-middleware
Author: BHou
