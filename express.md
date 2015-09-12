# Service: express

## Description
A wrapper of express. It is the object returned by

`````javascript
var express = require('express');

module.exports = express;
`````

## Usage
Reference the service in your plugin's package.json file:
`````json
{
  "plugin": {
    "consumes": [
      "express"
    ]
  }
}
`````

## Implementation

#### Plugin: fx-express
author: BHou
