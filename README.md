Tiny go program that reads 16- or 8-bit PCM aiff file and outputs 8-bit PCM data for Arduino.

### Usage

```
$ go run aiff2arduino.go [-dither] foo.aiff > foo.h
```

This generates a header file that looks like:

```
  prog_uchar foo[] PROGMEM = { 127, 127, ... };
```

which can be directly included in your Arduino code:

```
  #include "foo.h"
```

### References

* http://www-mmsp.ece.mcgill.ca/Documents/AudioFormats/AIFF/Docs/AIFF-1.3.pdf
* http://www-mmsp.ece.mcgill.ca/Documents/AudioFormats/AIFF/Docs/AIFF-C.9.26.91.pdf
