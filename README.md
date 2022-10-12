# L80 GPS module


This package adds functionality to the GPS breakout.

This is the Electronic Cats GPS makecode extension. Tested and works great with the L80 GPS module using MTK33x9 chipset

These modules use TTL serial to communicate, 2 pins are required to interface

Electronic Cats invests time and resources providing this open source design, please support Electronic Cats and open-source hardware by purchasing products from Electronic Cats!

This is modified for micro:bit by DoraLC. Funciton init() is added to set the pin connection. 
Direct to the original project: https://github.com/ElectronicCats/pxt-gps

## Usage
```
makerbit.connectLcd(39)
makerbit.setLcdBacklight(LcdBacklight.On)
makerbit.showStringOnLcd1602("hello", makerbit.position1602(LcdPosition1602.Pos1), 16)
gps.init(
SerialPin.P1,
SerialPin.P2,
BaudRate.BaudRate9600
)
basic.forever(function () {
    gps.encode()
    makerbit.showStringOnLcd1602("" + (gps.latitude()), makerbit.position1602(LcdPosition1602.Pos1), 16)
    makerbit.showStringOnLcd1602("" + (gps.longitude()), makerbit.position1602(LcdPosition1602.Pos17), 16)
})

```

## API

- `function init()` : initialize the module

- `function encode()` : encode sentence Nmea GPS  

- `function latitude()` : return latitude.

- `function longitude():` return longitude

- `function altitude()`: return altitude in meters.

- `function Date Time()`: return date and time UTC.


## License

MIT

Copyright (c) 2019, Electronic Cats  
Copyright (c) 2022, stem@eClass


## Supported targets

* for PXT/micro:bit

```package
l80
```

