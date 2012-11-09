# lynx

A minimalistic node.js client for [StatsD] server. Fork of original work by [sivy]

`lynx` features:

* **Minimalistic** — there is only a minimum of abstraction between you and 
  statsd
* **Re-usable UDP Connections** – Keeps UDP connections open for a certain time
* **Errors** - Pluggable error handling, by default errors are ignored

## Getting Started

```
$ npm install lynx
$ node
> var lynx = require('lynx')
> c = new lynx('localhost',8125)
{ host: 'localhost', port: 8125 }
> c.increment('node_test.int')
> c.decrement('node_test.int')
> c.timing('node_test.some_service.task.time', 500) // time in millis
```

## tests

Run the tests with `npm`.

``` sh
npm test
```

## meta

           `\.      ,/'
            |\\____//|
            )/_ `' _\(
           ,'/-`__'-\`\
           /. (_><_) ,\
           ` )/`--'\(`'  atc
             `      '

* code: `git clone git://github.com/dscape/lynx.git`
* home: <http://github.com/dscape/lynx>
* bugs: <http://github.com/dscape/lynx/issues>

`(oo)--',-` in [caos]

[caos]: http://caos.di.uminho.pt
[sivy]: https://github.com/sivy/node-statsd
[StatsD]: https://github.com/etsy/statsd
