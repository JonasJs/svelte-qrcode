# Svelte QrCode

[![npm version](https://badge.fury.io/js/svelte-qrcode.svg)](https://www.npmjs.com/package/svelte-qrcode)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/JonasJs/svelte-qrcode/blob/master/LICENSE)
[![Total alerts](https://img.shields.io/lgtm/alerts/g/JonasJs/svelte-qrcode.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/JonasJs/svelte-qrcode/alerts/)
[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/JonasJs/svelte-qrcode.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/JonasJs/svelte-qrcode/context:javascript)

Generate from QR Code with style, logo, and [Error Level Rate](https://blog.qrstuff.com/2011/12/14/qr-code-error-correction) that serve to avoid errors if the `QR Code` is damaged.

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

A example of how to use the library:

**[Example Repl](https://svelte.dev/repl/e9cee0cfb11c4cd1847e366209e8c907?version=3.22.3)**

```html
<script>
  import QrCode from "svelte-qrcode"
</script>

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


## Functions

### `getImage()`

Generates a base64 encoded data URI for the QR code.

// type = "image/png", quality = 1 

| Prop       | Type   | Description                                        | Default     |
| ---------- | ------ | -------------------------------------------------- | ----------- |
| type | String | Indicates the nature and format of a document                    | `image/png` |
| quality | Number | Exported image quality                    | `1` |



``` html
<script>
  import QrCode from "svelte-qrcode";

  let qrCodeRef;
  let value = "https://github.com/"

  function getImage() {
    /**
     * qrCodeRef.toDataURL
     * Params Default: { type = "image/png", quality = 1 }
     */
    const dataUrl = qrCodeRef.toDataURL();
    console.log(dataUrl);
  }
  
</script>

<div class="container">
  <QrCode value={value} bind:this={qrCodeRef} />

  <button on:click={getImage}>export</button>
</div>
```


## Faq

  - [QR Code Error Correction](https://blog.qrstuff.com/general/qr-code-error-correction).
  - [Quality Param](https://kangax.github.io/jstests/canvas_toDataURL_with_quality_param/).
  - [MIME types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types).
  


## NPM Statistics

Download stats for this NPM package

[![NPM](https://nodei.co/npm/svelte-qrcode.png)](https://nodei.co/npm/svelte-qrcode/)


## Bugs
If you have any problems with the Svelte QRious component raise an issue [here](https://github.com/JonasJs/svelte-qrcode/issues).

## License
**Svelte QrCode**
Copyright © 2022 Jonas Alves

**QRious**
Copyright © 2017 Alasdair Mercer  
Copyright © 2010 Tom Zerucha