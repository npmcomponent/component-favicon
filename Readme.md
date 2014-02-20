*This repository is a mirror of the [component](http://component.io) module [component/favicon](http://github.com/component/favicon). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-favicon`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# Favicon

  Dynamically change a favicon using a data uri string, typically
  from `canvas.toDataURL()`.

## Installation

```
$ component install component/favicon
```

## Example

 Count from 0 through 9:

```js
var icon = require('favicon');
var canvas = document.createElement('canvas');
canvas.width = canvas.height = 16;
var ctx = canvas.getContext('2d');
ctx.font = '16px Helvetica, Arial, sans-serif';

var nums = [0,1,2,3,4,5,6,7,8,9];
var i = 0;

setInterval(function(){
  ctx.clearRect(0, 0, 16, 16);
  var n = nums[i++ % 10];
  ctx.fillText(n, 0, 15);
  icon(canvas.toDataURL());
}, 300);
```

## API

### icon(string)

  Set the favicon to the given data uri `string`.

### icon.reset()

  Reset to the original favicon.

## License

  MIT
