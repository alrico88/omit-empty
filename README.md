# omit-empty [![NPM version](https://img.shields.io/npm/v/omit-empty.svg?style=flat)](https://www.npmjs.com/package/omit-empty) [![NPM downloads](https://img.shields.io/npm/dm/omit-empty.svg?style=flat)](https://npmjs.org/package/omit-empty) [![Build Status](https://img.shields.io/travis/jonschlinkert/omit-empty.svg?style=flat)](https://travis-ci.org/jonschlinkert/omit-empty)

Recursively omit empty properties from an object. Omits empty objects, arrays, strings or zero.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install omit-empty --save
```

## Usage

```js
var omitEmpty = require('omit-empty');

omitEmpty({a: 'a', b: ''});
//=> {a: 'a'}

omitEmpty({a: 'a', b: {c: 'c', d: ''}});
//=> {a: 'a', b: {c: 'c'}

omitEmpty({a: ['a'], b: []});
//=> {a: ['a']}

omitEmpty({a: 0, b: 1});
//=> {a: 0, b: 1}

// set the `noZero` flag
omitEmpty({a: 0, b: 1}, true);
//=> {b: 1}
```

## Related projects

You might also be interested in these projects:

* [for-in](https://www.npmjs.com/package/for-in): Iterate over the own and inherited enumerable properties of an objecte, and return an object… [more](https://www.npmjs.com/package/for-in) | [homepage](https://github.com/jonschlinkert/for-in)
* [for-own](https://www.npmjs.com/package/for-own): Iterate over the own enumerable properties of an object, and return an object with properties… [more](https://www.npmjs.com/package/for-own) | [homepage](https://github.com/jonschlinkert/for-own)
* [is-plain-object](https://www.npmjs.com/package/is-plain-object): Returns true if an object was created by the `Object` constructor. | [homepage](https://github.com/jonschlinkert/is-plain-object)
* [reduce-object](https://www.npmjs.com/package/reduce-object): Reduces an object to a value that is the accumulated result of running each property… [more](https://www.npmjs.com/package/reduce-object) | [homepage](https://github.com/jonschlinkert/reduce-object)

## Contributing

This document was generated by [verb](https://github.com/verbose/verb), please don't edit directly. Any changes to the readme must be made in [.verb.md](.verb.md). See [Building Docs](#building-docs).

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/omit-empty/issues/new).

## Building docs

Generate readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install -g verb verb-readme-generator && verb
```

## Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

## Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](https://github.com/jonschlinkert/omit-empty/blob/master/LICENSE).

***

_This file was generated by [verb](https://github.com/verbose/verb), v0.9.0, on June 01, 2016._