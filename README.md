# @tsiry/ui-identicon

Adapted from [Jazzicon](https://github.com/danfinlay/jazzicon) by Dan Finlay with the following changes -

- Random values now is read from the Uint8Array supplied (as opposed to having the seed as a number). This allows us to give an publicKey/address as an input and use those values in the pattern generation.
- Upgrade to the underlying [color](https://github.com/Qix-/color) library
- Generate circles as shapes (instead of rectangles)
- Interface updated to take in optional className & style
- Update everywhere to use ES6
- Split source into self-contained functions (TODO: future testing)
- Everything has been updated to use flow
- Test the library functions
- Copyright headers added (original also under ISC)

## Usage

```js
import identicon from '@tsiry/ui-identicon';

const publicKey = new Uint8Array([...]); // 32 bytes
const body = document.querySelector('body');
const identity = identicon(publicKey, 100 /* diameter, optional */, 'my-class' /* className, optional */ /* style. optional */ /* colors, optional */);

body.append(identity);
```

Also see [src/demo.js](src/demo.js) for a randomly generated example.

![demo](https://raw.githubusercontent.com/polkadot-js/ui/master/packages/ui-identicon/demo.png)
