# test dom
![tests](https://github.com/nichoth/debug/actions/workflows/nodejs.yml/badge.svg)
[![license](https://img.shields.io/badge/license-MIT-brightgreen)](LICENSE)

Tools for interacting with DOM elements

## install

```
npm i -D @nichoth/test-dom
```

## use

### commonjs
```js
const dom = require('@nichoth/test-dom')
```

### esm
```js
import { dom } from '@nichoth/test-dom'
```

## example

### waitForText
```js
const el = await dom.waitForText({
    // `dom.qs` is a convenience function, short for `document.querySelector`
    element: dom.qs('.css-query'),
    regex: /foo/
})
```

### waitFor
```js
const el = await dom.waitFor({
    // css query here
    selector: 'p'
})
```

### qs
```js
// document.querySelector
const el = dom.qs('#my-css-id')
```

### qsa
```js
// document.querySelectorAll
const elements = dom.qsa('.my-css-class')
```

### click
Automate click events

```js
const element = dom.qs('#example')
dom.click(element)
```

## test
```
npm test
```
