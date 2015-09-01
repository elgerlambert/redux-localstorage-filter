# redux-localstorage-filter
Storage enhancer to persist a subset of your state.

[![license](https://img.shields.io/npm/l/redux-localstorage-filter.svg?style=flat-square)](https://www.npmjs.com/package/redux-localstorage-filter)
[![npm version](https://img.shields.io/npm/v/redux-localstorage-filter.svg?style=flat-square)](https://www.npmjs.com/package/redux-localstorage-filter)
[![npm downloads](https://img.shields.io/npm/dm/redux-localstorage-filter.svg?style=flat-square)](https://www.npmjs.com/package/redux-localstorage-filter)

## Installation
```js
npm install --save redux-localstorage-filter
```

## Usage
```js
const storage = compose(
  filter('nested.key'),
)(adapter(localStorage));
```
For more information on using storage enhancers check out [redux-localstorage](elgerlambert/redux-localstorage)

## API
### filter(paths)
```js
type paths = Array<String> | String
```
A path is a `string` that points to the property key of your redux store that you would like to persist. In order to specify a nested key separate the keys that make up the full path with fullstops (`.`). Specify multiple paths by passing in an `Array`: 

```js
filter(['key', 'another.key']),
```

## License
MIT
