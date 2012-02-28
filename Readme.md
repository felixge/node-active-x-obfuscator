# active-x-obfuscator

A simple module to (safely) obfuscate all occurences of the string 'ActiveX'
inside some JavaScript code.

## Why?

Some coporate firewalls /proxys such as Blue Coat block JavaScript files to be
downloaded if they contain the word `'ActiveX'`. That of course is very annoying
for libraries such as [socket.io][] that need to use `ActiveXObject` for
supporting IE8 and older.

## Install

```
npm install active-x-obfuscator
```

## Usage

```js
var activeXObfuscator = require('active-x-obfuscator');
var code = 'foo(new ActiveXObject());';

var obfuscated = activeXObfuscator(code);
// -> foo(...)
```

## License

Licensed under the MIT license.

[socket.io]: http://socket.io/
