# to-ico [![Build Status](https://travis-ci.org/kevva/to-ico.svg?branch=master)](https://travis-ci.org/kevva/to-ico)

> Convert PNG to ICO in memory


## Install

```
$ npm install --save to-ico
```


## Usage

```js
const fs = require('fs');
const toIco = require('to-ico');

const files = [
	fs.readFileSync('unicorn-16x16.png'),
	fs.readFileSync('unicorn-32x32.png')
];

toIco(files).then(buf => {
	fs.writeFileSync('favicon.ico', buf);
});
```


## API

### toIco(input)

#### input

*Required*<br>
Type: `array`

An array of PNG image buffers.


## License

MIT © [Kevin Martensson](http://github.com/kevva)
