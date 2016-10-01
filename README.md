# es2040 [![stability][0]][1]
[![npm version][2]][3] [![downloads][8]][9] [![js-standard-style][10]][11]

`browserify` transform that compiles a selection of ES6 features to valid ES5:
- `fat arrows` - make inline functions cute-looking
- `template strings` / `tagged templates` - enable DSLs inside of JS
- `const` - using `const` by default makes it easy to spot where values are
  being redeclared
- `object destructuring` - `const { a, b } = { a: 1, b: 2 }`
- `array destructuring` - `const [a, b] = [1, 2]`
- `default parameters` - `({ a = 1, b = 2 } = {}) => a`
- `rest parameters` - `(a, b, ...args) => {}`
- `spread literals` - `f(a, b, ...args)`
- `short-hand properties` - `return { a, b }`
- `computed properties` - `return { [a]: b }`

Because, in hindsight, we can do without most of ES6.

Forked from [`es2020`](https://github.com/yoshuawuyts/es2020) for those of us with slightly worse vision.

## Usage
__Via `package.json` (recommended):__
```json
{
  "browserify": {
    "transform": [
      "es2040"
    ]
  }
}
```

__Via CLI:__
```js
$ browserify client.js -t es2040
```

__Via Node API:__
```js
const browserify = require('browserify')
browserify('./client.js')
  .transform('es2040')
  .bundle()
  .pipe(process.stdout)
```

## FAQ
### Is this a joke?
Not really. The TC39 does not represent my interests, and the features they
introduce are not useful for the stuff I'm doing.
[I'm](https://github.com/whatwg/streams)
[bloody](https://docs.google.com/presentation/d/1H3E2ToJ8VHgZS8eS6bRv-vg5OksObj5wv6gyzJJwOK0/edit)
[serious](https://github.com/whatwg/loader). A few good things have been
introduced, so that's what we're backporting to older browsers.

## Can you not?
If the TC39 had an open standards process perhaps this wasn't needed. But as it
stands they're an unwelcoming club, so I get to poke fun at this situation that
otherwise fills me with sadness. Feel free to poke fun at me too. Or if you're
angry that someone would make fun of _the hard work the TC39 has done_, feel
free to ignore this project. Do whatever, I'm doing the same.

## Can you include feature X?
Maybe. Open an issue, make a case and we can discuss it. Just remember that this
project is not democratically governed.

## Installation
```sh
$ npm install es2040
```

## See Also
- [babel-preset-es2040](https://github.com/ahdinosaur/babel-preset-es2040)
- [es2020](https://github.com/yoshuawuyts/es2020)

## License
[MIT](https://tldrlegal.com/license/mit-license)

[0]: https://img.shields.io/badge/stability-experimental-orange.svg?style=flat-square
[1]: https://nodejs.org/api/documentation.html#documentation_stability_index
[2]: https://img.shields.io/npm/v/es2040.svg?style=flat-square
[3]: https://npmjs.org/package/es2040
[4]: https://img.shields.io/travis/ahdinosaur/es2040/master.svg?style=flat-square
[5]: https://travis-ci.org/ahdinosaur/es2040
[6]: https://img.shields.io/codecov/c/github/ahdinosaur/es2040/master.svg?style=flat-square
[7]: https://codecov.io/github/ahdinosaur/es2040
[8]: http://img.shields.io/npm/dm/es2040.svg?style=flat-square
[9]: https://npmjs.org/package/es2040
[10]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[11]: https://github.com/feross/standard
