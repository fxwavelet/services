# Service: eventbus

## Description
An eventbus used to communicate between plugins. It avoids the dependencies between two communicating plugins

## Interface
*eventbus* is the service you get from *imports.eventbus*.

#### eventbus.emit(event, message)
Execute each of the listeners in order with the supplied arguments.

#### eventbus.on(event, handler)
Adds a listener to the end of the listeners array for the specified event.

#### eventbus.listeners(event)
Returns an array of listeners for the specified event.

#### eventbus.removeListener(event, listener)
Remove a listener from the listener array for the specified event.

## Example
`````javascript
var eventbus = imports.eventbus;

eventbus.on('hello', function(message) {
  console.log(message.code + ':' + message.data);
)

eventbus.emit('hello', {code: 200, data: 'OK'});
`````

output:
`````
200:OK
`````

Reference the service in your plugin's package.json file:
`````json
{
  "plugin": {
    "consumes": [
      "eventbus"
    ]
  }
}
`````

## Implementation

#### Plugin: fx-eventbus
author: BHou
