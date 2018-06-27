# sketch-fetch-complete(fork by skpm/sketch-polyfill-fetch)

A [fetch](https://developer.mozilla.org/en/docs/Web/API/Fetch_API) polyfill for sketch inspired by [unfetch](https://github.com/developit/unfetch). It is automatically included (when needed) when using [skpm](https://github.com/skpm/skpm).

## Installation

```bash
npm i -S sketch-fetch-complete
```

## Usage

```js
const fetch = require('sketch-fetch-complete')

fetch("https://google.com")
  .then(response => response.text())
  .then(text => console.log(text))
  .catch(e => console.error(e))
```

## extra add

upload file

```js
const fetch = require('sketch-fetch-complete')

fetch("https://google.com", {
  method: 'post',
  formdata: {
    files: [path],
    ...objects,
  }
})
  .then(response => response.json())
  .then(text => console.log(text))
  .catch(e => console.error(e))
```

