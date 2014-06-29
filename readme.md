# ffmpeg-win

Encode flac, mp3, opus and wav files on Windows with <a href="http://ffmpeg.zeranoe.com/builds/" target="_blank">ffmpeg version git-10012fa (2014-06-14) 64bit</a>

No option, just best quality

## Install

Install with <a href="http://nodejs.org/" target="_blank">npm</a> directly from the <a href="https://github.com/jeromedecoster/ffmpeg-win" target="_blank">github repository</a>

```
npm install --save-dev jeromedecoster/ffmpeg-win
```

## API

```js
flac(src, dest, cb(err));
mp3(src, dest, cb(err));
opus(src, dest, cb(err));
wav(src, dest, cb(err));
```

or

```js
flac(src, cb(err));
mp3(src, cb(err));
opus(src, cb(err));
wav(src, cb(err));
```

## Example

```js
var ffmpeg = require('ffmpeg-win');

function done(err) {
  if (err) throw err;
  console.log('ok, done');
}

ffmpeg.mp3('./source.wav', done);
```

or

```js
var ffmpeg = require('ffmpeg-win');

function done(err) {
  if (err) throw err;
  console.log('ok, done');
}

ffmpeg.opus('./source.mp3', './dest.opus', done);
```
