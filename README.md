# node-vimeo-downloader

Yet another vimeo downloading module. This time written with only Javascript and a more node-friendly streaming interface.

[![Build Status](https://secure.travis-ci.org/fent/node-ytdl-core.svg)](http://travis-ci.org/fent/node-ytdl-core)
[![Dependency Status](https://gemnasium.com/fent/node-ytdl-core.svg)](https://gemnasium.com/fent/node-ytdl-core)
[![codecov](https://codecov.io/gh/fent/node-ytdl-core/branch/master/graph/badge.svg)](https://codecov.io/gh/fent/node-ytdl-core)


# Usage

```js
var fs = require('fs');
var vidl = require('vimeo-downloader');

vidl('https://vimeo.com/183482793')
  .pipe(fs.createWriteStream('video.flv'));
```


# API
### ytdl(url, options)

Attempts to download a video from the given url. Returns a readable stream. `options` can have the following keys

* `quality` - Video quality to download. a list of values are `highest`, `medium`, `lowest` or  resolution tag liek 360p, 144p etc..
* `format` - Default it download the mp4 format

```js
// Example with `filter` option.
vidl(url, { quality: '360p' })
  .pipe(fs.createWriteStream('vide.mp4'));
```


# Install

    npm install vimeo-downloader


# License
MIT