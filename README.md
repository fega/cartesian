# Cartesian
Computes the cartesian product of arrays provided by an array or an object

Is a clone of the cartesian packages, but this contains NO DEPENDENCIES.

## Install

```
npm install @fega/cartesian --save
```

## Examples

```javascript
var cartesian = require('@fega/cartesian');
```

### Array or arrays:

```javascript
cartesian([
  ['A', 'B', 'C'],
  ['M'],
  ['X', 'Y'],
  'Z'
]);

// =>
// [
//   [ 'A', 'M', 'X', 'Z' ],
//   [ 'A', 'M', 'Y', 'Z' ],
//   [ 'B', 'M', 'X', 'Z' ],
//   [ 'B', 'M', 'Y', 'Z' ],
//   [ 'C', 'M', 'X', 'Z' ],
//   [ 'C', 'M', 'Y', 'Z' ]
// ]
```

### Object with array properties:

```javascript
cartesian({
  cdn  : ['image1', 'image2'],
  path : '/dir',
  files: ['file1', 'file2', 'file3']
});

// =>
// [
//   { cdn: 'image1', path: '/dir', files: 'file1' },
//   { cdn: 'image1', path: '/dir', files: 'file2' },
//   { cdn: 'image1', path: '/dir', files: 'file3' },
//   { cdn: 'image2', path: '/dir', files: 'file1' },
//   { cdn: 'image2', path: '/dir', files: 'file2' },
//   { cdn: 'image2', path: '/dir', files: 'file3' }
// ]
```

For more examples check out [`test.js`](test.js).

## License

[MIT](LICENSE)
