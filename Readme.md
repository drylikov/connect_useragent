# connect_useragent

  A tiny Connect user-agent middleware exposing user-agent details to your application and views. A good idea by @guille backed by @3rd-Eden's [useragent](https://github.com/3rd-Eden/useragent) module.

## Installation

    $ npm install connect_useragent

## Example

```js
var connect = require('connect')
  , useragent = require('connect_useragent');

connect()
  .use(connect.logger('dev'))
  .use(useragent())
  .use(function(req, res){
    console.log(req.agent);
  })
  .listen(3000);
```

provides details such as the following:

```js
{ family: { name: 'Safari', machine: 'safari' },
  major: '5',
  minor: '0',
  patch: '4',
  os: { name: 'Mac OS X', machine: 'mac-os-x' } }
```











