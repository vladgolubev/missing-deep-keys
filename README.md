# Missing Deep Keys

> Tells what keys from first object are missing in second

## Install

Ensure you have [Node.js](https://nodejs.org) version 4 or higher installed. Then run the following:

```
$ npm install missing-deep-keys --save
```

## Usage

```javascript
const o1 = {a: {b: 2}}; // Base object
const o2 = {c: 1}; // Comparison object

const result = missingDeepKeys(o1, o2);

// Prints keys present in o1 but missing in o2
console.log(result); // => ['a.b']
```

## API

### missingDeepKeys(o1, o2, [showIntermediate])

Returns an array of keys present in o1 but missing in o2

#### o1
#### o2

| Type   | Default |
|--------|---------|
| Object | `{}`    |

### showIntermediate

| Type    | Default |
|---------|---------|
| Boolean | `false` |

Additionally returns a parent object if its children are missing.

From the example above:

```javascript
// ...
missingDeepKeys(o1, o2, false); // => ['a.b']
missingDeepKeys(o1, o2, true); // => ['a', 'a.b']
```

## Tests

```
$ npm run test
```

## License

MIT © [Vlad Holubiev](https://github.com/vladgolubev)
