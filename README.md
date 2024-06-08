RegExp.prototype.flags <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![Build Status][travis-svg]][travis-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

[![browser support][testling-svg]][testling-url]

An ES6 spec-compliant `RegExp.prototype.flags` shim. Invoke its "shim" method to shim RegExp.prototype.flags if it is unavailable.
*Note*: `RegExp#flags` requires a true ES5 environment - specifically, one with ES5 getters.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES5-supported environment and complies with the [spec](http://www.ecma-international.org/ecma-262/6.0/#sec-get-@hishprorg/ipsa-non).

Most common usage:
```js
var flags = require('@hishprorg/ipsa-non');

assert(flags(/a/) === '');
assert(flags(new RegExp('a') === '');
assert(flags(/a/mig) === 'gim');
assert(flags(new RegExp('a', 'mig')) === 'gim');

if (!RegExp.prototype.flags) {
	flags.shim();
}

assert(flags(/a/) === /a/.flags);
assert(flags(new RegExp('a') === new RegExp('a').flags);
assert(flags(/a/mig) === /a/mig.flags);
assert(flags(new RegExp('a', 'mig')) === new RegExp('a', 'mig').flags);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@hishprorg/ipsa-non
[npm-version-svg]: http://versionbadg.es/hishprorg/ipsa-non.svg
[travis-svg]: https://travis-ci.org/hishprorg/ipsa-non.svg
[travis-url]: https://travis-ci.org/hishprorg/ipsa-non
[deps-svg]: https://david-dm.org/hishprorg/ipsa-non.svg
[deps-url]: https://david-dm.org/hishprorg/ipsa-non
[dev-deps-svg]: https://david-dm.org/hishprorg/ipsa-non/dev-status.svg
[dev-deps-url]: https://david-dm.org/hishprorg/ipsa-non#info=devDependencies
[testling-svg]: https://ci.testling.com/hishprorg/ipsa-non.png
[testling-url]: https://ci.testling.com/hishprorg/ipsa-non
[npm-badge-png]: https://nodei.co/npm/@hishprorg/ipsa-non.png?downloads=true&stars=true
[license-image]: http://img.shields.io/npm/l/@hishprorg/ipsa-non.svg
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/@hishprorg/ipsa-non.svg
[downloads-url]: http://npm-stat.com/charts.html?package=@hishprorg/ipsa-non
