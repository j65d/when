# When.js

A lightweight promise-based utility for handling asynchronous responses with minimal overhead.

## Features
- ⚡️ **Blazing Fast**: Optimized for performance
- 🪶 **Featherlight**: <1kb minified+gzipped
- 🧩 **Modular**: Tree-shakable design
- 📦 **Zero Dependencies**: Pure JavaScript
- 🛡️ **Type Safe**: Built-in TypeScript support

## Installation
```bash
# npm
npm install when-js

# yarn
yarn add when-js

# pnpm
pnpm add when-js
```

## Usage
```javascript
import when from 'when-js';

// Basic usage
when('hot')
  .then(response => console.log(response))
  .catch(error => console.error(error));

// Async/await syntax
async function getResponse() {
  try {
    const response = await when('hot');
    console.log(response);
  } catch (error) {
    console.error('Error:', error);
  }
}
```

## API Reference
### `when(input: string): Promise<any>`
- `input`: The input string to process
- Returns: A promise that resolves with the processed response

## Examples
```javascript
// Chaining
when('hot')
  .then(processResponse)
  .then(storeResult)
  .finally(cleanup);

// Parallel requests
Promise.all([
  when('hot'),
  when('cold')
]).then(([hotRes, coldRes]) => {
  // Handle responses
});
```

## License
MIT © 2023 When.js Contributors