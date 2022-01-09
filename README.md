# banglejs-2-hollow-clock-hands #

draws (optionally filled) hollow hands for an analog clock on a Bangle.js 2

This module draws (optionally filled) hollow hands for an analog clock running on a [Bangle.js 2](https://www.espruino.com/Bangle.js2).

## Usage ##

Within a clock implementation, the module may be used as follows:

```
let ClockHands = require('https://raw.githubusercontent.com/rozek/banglejs-2-hollow-clock-hands/main/ClockHands.js');
```

Whenever needed, the module's exported `draw` method will then be invoked as follows:

```
ClockHands.draw(Settings, CenterX,CenterY, outerRadius, Hours,Minutes,Seconds);
```

The `Seconds` argument is optional and may be missing (or set to `null` or `undefined`) - in that case no seconds hands should be drawn.

`Settings.FillColor` controls whether hour and mionute hands will be filled or not:

* `null`, `undefined` or missing: hands will *not* be filled,
* `'Theme'`: hands will be filled with the current theme's foreground highlight color (`theme.fgH`)
* (color): any valid Espruino color specification fills the hands with that color

## License ##

[MIT License](LICENSE.md)
