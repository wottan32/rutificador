# rutificador
[![npm version][npm-image]][npm-url] [![Build Status][ci-image]][ci-url] [![dependencies][dependencies-image]][dependencies-url] [![lint][lint-image]][lint-url]

> Disclamer: This is made with learning purposes, use by your own responsability.

## Install
This project uses ES6, so make sure your [Node version is compatible](https://nodejs.org/en/docs/es6/).
```sh
$ npm install --save rutificador
```

## Usage
```js
'use strict';

const rutificador = require('rutificador');

rutificador({name: 'Juán Perez'}).then(juanitos => {
  console.log(juanitos);
}).catch(err => {
  // Do something
});
```

This prints:
```js
[ { name: 'JUAN PEREZ DUQUE', rut: 'XXXXXXX-6' },
  { name: 'RAUL JUAN PEREZ MONTENEGRO', rut: 'XXXXXXX-0' },
  { name: 'JUAN PEREZ ROJAS', rut: 'XXXXXXX-6' },
  ... ]
```

Also you can match by RUT:
```js
rutificador({rut: 'XXXXXXX-0'}).then(resp => {
  // ...
});
```

[ci-image]: https://travis-ci.org/mrpatiwi/rutificador.svg
[ci-url]: https://travis-ci.org/mrpatiwi/rutificador
[npm-image]: https://badge.fury.io/js/rutificador.svg
[npm-url]: http://badge.fury.io/js/rutificador
[dependencies-image]: https://david-dm.org/mrpatiwi/rutificador.svg
[dependencies-url]: https://david-dm.org/mrpatiwi/rutificador
[lint-image]: https://codeclimate.com/github/mrpatiwi/rutificador/badges/gpa.svg
[lint-url]: https://codeclimate.com/github/mrpatiwi/rutificador
