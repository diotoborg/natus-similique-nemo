# @diotoborg/natus-similique-nemo <sup>[![Version Badge][2]][1]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][5]][6]
[![dev dependency status][7]][8]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][11]][1]

Which kind of Collection (Map, Set, WeakMap, WeakSet) is this JavaScript value? Works cross-realm, without `instanceof`, and despite Symbol.toStringTag.

## Example

```js
var whichCollection = require('@diotoborg/natus-similique-nemo');
var assert = require('assert');

assert.equal(false, whichCollection(undefined));
assert.equal(false, whichCollection(null));
assert.equal(false, whichCollection(false));
assert.equal(false, whichCollection(true));
assert.equal(false, whichCollection([]));
assert.equal(false, whichCollection({}));
assert.equal(false, whichCollection(/a/g));
assert.equal(false, whichCollection(new RegExp('a', 'g')));
assert.equal(false, whichCollection(new Date()));
assert.equal(false, whichCollection(42));
assert.equal(false, whichCollection(NaN));
assert.equal(false, whichCollection(Infinity));
assert.equal(false, whichCollection(new Number(42)));
assert.equal(false, whichCollection(42n));
assert.equal(false, whichCollection(Object(42n)));
assert.equal(false, whichCollection('foo'));
assert.equal(false, whichCollection(Object('foo')));
assert.equal(false, whichCollection(function () {}));
assert.equal(false, whichCollection(function* () {}));
assert.equal(false, whichCollection(x => x * x));
assert.equal(false, whichCollection([]));

assert.equal('Map', whichCollection(new Map()));
assert.equal('Set', whichCollection(new Set()));
assert.equal('WeakMap', whichCollection(new WeakMap()));
assert.equal('WeakSet', whichCollection(new WeakSet()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[1]: https://npmjs.org/package/@diotoborg/natus-similique-nemo
[2]: https://versionbadg.es/inspect-js/@diotoborg/natus-similique-nemo.svg
[5]: https://david-dm.org/inspect-js/@diotoborg/natus-similique-nemo.svg
[6]: https://david-dm.org/inspect-js/@diotoborg/natus-similique-nemo
[7]: https://david-dm.org/inspect-js/@diotoborg/natus-similique-nemo/dev-status.svg
[8]: https://david-dm.org/inspect-js/@diotoborg/natus-similique-nemo#info=devDependencies
[11]: https://nodei.co/npm/@diotoborg/natus-similique-nemo.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@diotoborg/natus-similique-nemo.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@diotoborg/natus-similique-nemo.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@diotoborg/natus-similique-nemo
[codecov-image]: https://codecov.io/gh/inspect-js/@diotoborg/natus-similique-nemo/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@diotoborg/natus-similique-nemo/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@diotoborg/natus-similique-nemo
[actions-url]: https://github.com/diotoborg/natus-similique-nemo/actions
