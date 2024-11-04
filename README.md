<div align="center">

# `svelte-qrcode`


[![npm version](https://badge.fury.io/js/svelte-qrcode.svg)](https://www.npmjs.com/package/svelte-qrcode)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/JonasJs/svelte-qrcode/blob/master/LICENSE)


QR Code generator for <b>Svelte</b> & <b>SvelteKit</b> with style, logo, and [Error Level Rate](https://blog.qrstuff.com/2011/12/14/qr-code-error-correction) that serve to avoid errors if the `QR Code` is damaged.

</div>



## Installation

```
npm i svelte-qrcode
// OR
yarn add svelte-qrcode
```

## Demo [Link](https://svelte-qrcode.now.sh/)

![image](https://user-images.githubusercontent.com/11879767/82413216-59eab480-9a4b-11ea-816c-019bc7f63a34.png)

Local demo:

```
git clone https://github.com/JonasJs/svelte-qrcode.git
cd svelte-qrcode
yarn install && yarn start
```

## Examples

An example of how to use the library:

**[Example Repl](https://svelte.dev/repl/e9cee0cfb11c4cd1847e366209e8c907?version=5.1.9)**

```js
<script>import QrCode from "svelte-qrcode"</script>
```

```html
<div class="container">
  <QrCode value="https://github.com/" />
</div>
```

## Properties

You can control many aspects of the QR code using the following props:

| Prop       | Type   | Description                                        | Default     |
| ---------- | ------ | -------------------------------------------------- | ----------- |
| background | String | Background color of the QR code                    | `"#FFFFFF"` |
| color | String | Foreground color of the QR code                    | `"#000000"` |
| errorCorrection      | String | Error correction level of the QR code (L, M, Q, H) | `"L"`       |
| padding    | Number | Padding for the QR code (pixels)                   | `0`         |
| size       | Number | Size of the QR code (pixels)                       | `200`       |
| value      | String | Value encoded within the QR code                   | `""`        |

## NPM Statistics

Download stats for this NPM package

[![NPM](https://nodei.co/npm/svelte-qrcode.png)](https://nodei.co/npm/svelte-qrcode/)

## License

Svelte Adress Autocomplete is open source software [licensed as MIT](https://github.com/JonasJs/svelte-qrcode/blob/master/LICENSEE).
