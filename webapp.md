# Service: webapp

## Description
A wrapper of expressjs. It is the object returned by

`````javascript
var express = require('express');

var webapp = express();

module.exports = webapp;
`````

## Usage
Reference the service in your plugin's package.json file:
`````json
{
  "plugin": {
    "consumes": [
      "webapp"
    ]
  }
}
`````

## Implementation

#### Plugin: fx-express
author: BHou
