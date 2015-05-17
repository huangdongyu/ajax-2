# Ajax
> Ajax module in Vanilla JS

<img align="right" src="ajax-logo.png" alt="Ajax" />

[![Build Status][travis-image]][travis-url]
[![Coveralls Coverage Status][coverage-image]][coverage-url]
[![Code Climate Coverage][codeclimate-coverage-image]][codeclimate-coverage-url]
[![Code Climate][codeclimate-image]][codeclimate-url]
[![License][license-image]][license-url]
[![CONTRIBUTING][contributing-image]][contributing-url]

### Methods

#### `get(url)`

> Get data as a JSON object.

```js
var ajax = new Ajax();
ajax.get( '/api/users' );
```

#### `post(url, [ data ])`

> Save a new register.

```js
var ajax = new Ajax();
ajax.post( '/api/users', { data: 'value' });
```

#### `put(url, [ data ])`

> Upgrade part of a register.

```js
var ajax = new Ajax();
ajax.put( '/api/users', { slug: 'john' });
```

#### `delete(url, [ data ])`

> Delete a register.

```js
var ajax = new Ajax();
ajax.delete( '/api/users', { id: 1 });
```

### Return methods

#### `done(response, xhrObject)`

> Promise that returns if the request was successful.

```js
var ajax = new Ajax();
ajax.get( '/api/users' ).done(function( response, xhr ) {
  // Do something
});
```

#### `error(response, xhrObject)`

> Promise that returns if the request has an error.

```js
var ajax = new Ajax();
ajax.post( '/api/users', { slug: 'john' }).error(function( response, xhr ) {
  // Do something
});
```

#### `always(response, xhrObject)`

> That promise always returns, independent if the status is `done` or `error`.

```js
var ajax = new Ajax();
ajax.post( '/api/users', { slug: 'john' }).always(function( response, xhr ) {
  // Do something
});
```

### Contributing

Check [CONTRIBUTING.md][contributing-url]

### Code coverage and Statistics

<https://github.com/reportz/ajax>

### License

[MIT][license-url] © Fernando Daciuk

[travis-image]: https://img.shields.io/travis/fdaciuk/ajax.svg?style=flat-square
[travis-url]: https://travis-ci.org/fdaciuk/ajax
[coverage-image]: https://img.shields.io/coveralls/fdaciuk/ajax/master.svg?style=flat-square
[coverage-url]: https://coveralls.io/r/fdaciuk/ajax?branch=master
[codeclimate-coverage-image]: https://img.shields.io/codeclimate/coverage/github/fdaciuk/ajax.svg?style=flat-square
[codeclimate-coverage-url]: https://codeclimate.com/github/fdaciuk/ajax
[codeclimate-image]: https://img.shields.io/codeclimate/github/fdaciuk/ajax.svg?style=flat-square
[codeclimate-url]: https://codeclimate.com/github/fdaciuk/ajax
[license-image]: https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square
[license-url]: https://github.com/fdaciuk/licenses/blob/master/MIT-LICENSE.md
[contributing-image]: https://img.shields.io/badge/fdaciuk%2Fajax-CONTRIBUTE-orange.svg?style=flat-square
[contributing-url]: CONTRIBUTING.md