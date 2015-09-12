# Service: logger

## Description
**Wavelet** logger service

## Interface
*Logger* is the service you get from *imports.logger*

#### getLogger(moduleName)
return logger instance with module name

the logger instance from the interface *getLogger*

- logger.info(...);

- logger.warn(...);

- logger.error(...);

## Example
`````javascript
var Logger = imports.logger;
var logger = Logger.getInstance('ModuleName');

logger.info('hello world', 'Anonymous', '!');
logger.warn('hello world!', 'Anonymous', '!!');
logger.error('hello world!', 'Anonymous', '!!!');
`````

## Implementation
#### Plugin: fx-logger
author: BHou
