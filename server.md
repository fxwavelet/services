# Service: server

## Description
A wrapper of nodejs http server. It is the object returned by following code:

`````javascript
var server = http.createServer(webapp);

module.exports = server;
`````
## Usage
Reference the service in your plugin's package.json file:
`````json
{
  "plugin": {
    "consumes": [
      "server"
    ]
  }
}
`````

## Implementation

#### Plugin: fx-express
author: BHou
