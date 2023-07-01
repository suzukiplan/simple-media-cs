# Simple Media I/O Class Library

## About

NET Core is a simple class library that can be used to simply output uncompressed multimedia files (.bmp, .wav).

## Pre-request

- .NET Core 7.0
  - _Since only basically functions are used, it is expected to work fine before 6.0._

## How to build

```
dotnet build
```

## Class Specification

### SimpleBitmap

```c#
SimpleBitmap bmp = new SimpleBitmap(width, height);
bmp.SetPixel(x, y, red, green, blue); // red, green, blue = 0~255
bmp.SetPixelRGB565(x, y, rgb565); // rgb565 = 0bRRRRRGGGGGGBBBBB
bmp.WriteFile("/path/to/graphic.bmp");
```

### SimpleWave

```c#
SimpleWave wav = new SimpleWave(44100, 16, 2); // samling-rate, bit-rate, channels
wav.Append(pcm); // append byte array
wav.WriteFile("/path/to/sound.wav");
```

## License

[MIT](LICENSE.txt)
