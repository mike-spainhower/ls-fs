# ls-fs [![Build Status](https://travis-ci.org/LiveSafe/ls-fs.svg?branch=master)](https://travis-ci.org/LiveSafe/ls-fs)

File utils

![Snuffles](http://1.bp.blogspot.com/-xA9Da55eN9s/Up8S5jZzzVI/AAAAAAAAp4s/kJMdPIQblvE/s1600/SNUFFLES+MINE+BENTLEY.png)

## Usage

```js
var lsFs = require('ls-fs');

lsFs.readJson('settings.json').then(function(settings) {
    console.log(settings.prop1);
    console.log(settings.prop2);
});
```

## API

### readJson

```js
lsFs.readJson(path, [opts]).then(function(parsedJsonObj) {
    console.log(parsedJsonObj);
});
```

###### Arguments

1. `path` _(String)_ The path to the JSON file to read


### writeJson

```js
lsFs.writeJson(path, obj, [opts]).then(function(pathToJson) {
    
});
```

###### Arguments

1. `path` _(String)_ The path to the JSON file to write
1. `obj` _(*)_ The thing to JSON.stringify


### tmpDir

```js
lsFs.tmpDir([opts]).then(function(pathToTmpDir) {
    // do stuff with my temporary directory
});
```

###### Arguments

1. `[opts]` _(Object)_ Same as https://github.com/raszi/node-tmp#directory-creation

