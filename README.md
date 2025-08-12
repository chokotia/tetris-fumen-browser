# tetris-fumen-browser

Browser version of [tetris-fumen](https://github.com/knewjade/tetris-fumen) v1.1.3.

## Usage

```html
<script src="https://cdn.jsdelivr.net/gh/chokotia/tetris-fumen-browser/dist/tetris-fumen.min.js"></script>
<script>
  const { decoder, encoder } = TetrisFumen;
  
  // Decode fumen
  const pages = decoder.decode('v115@vhAAgH');
  console.log(pages[0].field.str());
  
  // Encode fumen
  const data = encoder.encode(pages);
  console.log(data);
</script>
```

## About

The original tetris-fumen package is Node.js only. This provides a browser-compatible build using webpack.

## Build

```bash
# Setup project
mkdir tetris-fumen-browser
cd tetris-fumen-browser
npm init -y

# Install dependencies
npm install tetris-fumen@1.1.3 webpack webpack-cli

# Create bundle
npx webpack --entry ./node_modules/tetris-fumen/index.js --output-path ./dist --output-filename tetris-fumen.min.js --output-library-name TetrisFumen --output-library-type umd --mode production
```

## License

MIT - Same as original [tetris-fumen](https://github.com/knewjade/tetris-fumen) by knewjade.