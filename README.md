# ESP32 TFT Weather
Hardware Required:
- ESP32 (Arduino UNO style board so it is compatible with the shield). I bought this [Hailege UNO R32](https://www.amazon.co.uk/gp/product/B07XGGMK3F/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) one that is based on a Wesmos R32.

# Hardware Setup
## Driver install
I used this one from the manufacturer as the version Windows update provides didn't work for me:
https://www.wch.cn/downloads/CH341SER_ZIP.html

## Install graphics library
TFT_eSPI provides us with all the good stuff and more, just like Adafruit does for Arduino.

[TFT_eSPI Library](https://github.com/Bodmer/TFT_eSPI#8-bit-parallel-support)

But, the easiest way to download it is via the Arduino IDE.

## Soldering
As the pin layout of the board is slightly different (exposes analog pins) to the Arduino, you need to do a bit of soldering.

Details here: https://github.com/Bodmer/TFT_eSPI#8-bit-parallel-support

![New wires](https://camo.githubusercontent.com/41b0878c288f290e30b53f26960dc33886dce3e8d2c418431c180fdad3e0796c/68747470733a2f2f692e696d6775722e636f6d2f70555a6e366c462e6a7067 "Solder some new wires")

## New pin setup
Due to the aforementioned modification, you also need to modify the graphics library to make use of the new pins:
Edit: `C:\Users\%username%\Documents\Arduino\libraries\TFT_eSPI\User_Setup_Select.h` (path varies per system)
and uncomment: `#include <User_Setups/Setup14_ILI9341_Parallel.h>  // Setup file for the ESP32 with parallel bus TFT`

# Software Setup
TODO: This repo!

You can now write code for the esp32 and display content on the screen!

but also: you can just run one of the examples found via the Arduino IDE, upload the code and done!