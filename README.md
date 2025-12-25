# PhotoPainter (B) firmware

Opinionated adaptation of the [WaveShare PhotoPainter B official firmware](https://github.com/waveshareteam/PhotoPainter_B).

The firmware assumes you have your pictures set up in a `pic` folder with `%04d.bmp` naming: 0001.bmp, 0002.bmp etc.

Approximately every hour a new random picture is chosen. Starting with random between 1 and 9999 and winding down to a smaller range based on when a file is not found. This means that initially the updates will be a tiny bit slower, but speed up over time.

## The NEXT button
The NEXT button will cause the next update round to update the display (possibly a 5 seconds later then pressing the button).
If the NEXT button is pressed more than 4 times during the 5 second sleep, the display will reboot.

## Build
```
cmake .
make
```

uf2 file can be found in the `target` folder.
