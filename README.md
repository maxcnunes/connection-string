connection-string
=================

URL Connection String Parser - _for all browsers and Node.js versions._

[![Build Status](https://travis-ci.org/vitaly-t/connection-string.svg?branch=master)](https://travis-ci.org/vitaly-t/connection-string)
[![Coverage Status](https://coveralls.io/repos/vitaly-t/connection-string/badge.svg?branch=master)](https://coveralls.io/r/vitaly-t/connection-string?branch=master)

Accepts a URL connection string (with every element being optional): 

```
protocol://user:password@hostname:12345/segment1/segment2?param1=value1&param2=value2
```

and converts it into an object:

```js
{
    protocol: 'protocol',
    user: 'user',
    password: 'password',
    host: 'hostname:12345',
    hostname: 'hostname',
    port: 12345,
    segments: ['segment1', 'segment2'],
    params: {
        param1: 'value1',
        param2: 'value2'
    }
}
```

Only those properties are set that are present in the connection string.

## Installing

```
$ npm install connection-string
```

## Usage

* **Node.js**

```js
var parse = require('connection-string');
var obj = parse('my-server:12345');
```

* **Browser**

```html
<script src="./connection-string"></script>

<script>
    var obj = parseConnectionString('my-server:12345');
</script>
```

For details and examples see the [WiKi Pages](https://github.com/vitaly-t/connection-string/wiki).
