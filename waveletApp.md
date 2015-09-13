# Service: waveletApp

## Description
The web app with middleware and NodeRED inited. Consume this service if you want to use express web application.

The difference between **waveletApp** service and **webapp** service:

- webapp service is simply the express application without applying any middleware and NodeRED
- waveletApp service applies the middlewares defined in **middlewares** service, and initiate NodeRED

## Example
`````javascript
var waveletApp = imports.waveletApp;

waveletApp.use('/hello', function(req, res) {
    res.end('Hello World');
});
`````

## Usage
Reference the service in your plugin's package.json file:
`````json
{
  "plugin": {
    "consumes": [
      "waveletApp"
    ]
  }
}
`````

## Implementation

#### Wavelet installation implements this service