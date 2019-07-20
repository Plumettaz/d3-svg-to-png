#d3-svg-to-png

Converts SVG elements to PNG and other image formats while keeping CSS styles. Optionally, it returns the data as a promise ordownloads it. It can also rescale the svg image.

## Installation

```shell
$ npm i d3-svg-to-png
```

## Usage

```js
const d3ToPng = require('d3-svg-to-png');
d3ToPng('selector', 'name');
```

## Mandatory fields

- **Selector** (String): Commonly 'svg';
- **Name** (String): Name for the file output, without extension.

Output: **name.png**

## Options

```js
const d3ToPng = require('d3-svg-to-png');
d3ToPng('svg', 'name', { scale: 3, format: 'webp', quality: 0.01, download: false, ignore: '.ignored' }).then(fileData => {
  //do something with the data
});
```

- **scale** (number): Rescale the image by this factor. Default: _1_
- **format** (string): The format to output to. Compatibility might vary between browsers. See [HTMLCanvasElement.toDataURL()
  ](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/toDataURL). Default: _png_
- **quality** (number): Between 0 (lowest) and 1. Affects formats with compression, like jpg. Default: _.92_
- **download** (boolean): Wether to download the resulting image. Default: _true_
- **ignore** (string): A CSS selector that, the matched elements of which will not me added to the output. Default: _null_

## Notes

Please report any problem, as this has not been thoroughly tested and could be improved.

## TODO

- Add feature to remove a class of elements, optionally