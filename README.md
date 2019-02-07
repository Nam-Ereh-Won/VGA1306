This is the start of a modification that will offer greater color options via use of R-2R Ladders for each of the output pins.

The primary purpose is to enhance the DMG implementation's feature set with the following functions listed by order of priority:

- Green monochrome DMG palette.
- Black monochrome GBP palette.
- Means to switch palettes without necessitating reburning.
- All but 2 of the 32 SGB palettes. The prior two will take their place.
- Trick games into thinking the console is SGB.
- Make use of regional palettes for games that support full color on SGB.
- Display a generic border around the game screen.
- Display game specific borders around the game screen.

http://gbdev.gg8.se/wiki/articles/SGB_Functions

If I am interpretting the documentation correctly, SGB functionality merely requries tapping into the 6 pins used for the joystick and interpretting the necessary codes for the SGB functions needed. The most important one is the MLT_REQ command which requires writing Joystick IDs to the lower 4 bits via P10-P13. P14 and P15 are needed to receive commands and data.




Original README here.

# VGA1306 (VGA-out for DIY Arduboys implemented on an FPGA!)

VGA1306.v & VGA1306.pcf are for the SSD1306 Emulation (4x scaling of the 128x64 frame)

VGA1306_640x320 is a variation of the SSD1306 Emulation (5x scaling of the 128x64 frame)

---

DMG1306.v & DMG1306.pcf are for the GameBoy VGA-out Implementation!

---

VGA1306_CS.v & VGA1306_CS.pcf are a variation of the SSD1306 Emulation, allowing for correct use of the CS (chip select) pin, in case there are other devices sharing the SPI bus

VGA1306_V.v & VGA1306_V.pcf are another variation of the SSD1306 Emulation, allowing for 'vertical addressing' as used by: https://github.com/notro/fbtft/blob/master/fb_ssd1306.c

VGA1106.v & VGA1106.pcf are an 'SH1106-friendly' variation, using the 0xB0 'page addressing' command for VSYNC
