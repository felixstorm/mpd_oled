# Fork of https://github.com/antiprism/mpd_oled

## Changes (targeted to my personal use case in a children's music player)
* No spectrum, just infos (spectrum does not seem to work with VolumIO Spotify anyway and would probably consume quite some CPU power on a Raspberry Pi Zero)
* Rearranged display to personal taste
* Display timeout when in paused state (3 minutes)
* A few minor enhancements

---

# Moode, Volumio, RuneAudio and MPD OLED Spectrum Display for Raspberry Pi

The mpd_oled program displays an information screen including a music
frequency spectrum on an OLED screen connected to a Raspberry Pi (or similar)
running MPD, this includes Moode, Volumio and RuneAudio.
The program supports I2C and SPI 128x64 OLED displays with an SSD1306,
SSD1309, SH1106 or SSH1106 controller.
![OLED with mpd_oled](mpd_oled.jpg)

## Build and install

The instructions depend on the player

* [Build and install on Volumio](INSTALL_VOLUMIO.md)
* [Build and install on Moode](INSTALL_MOODE.md)
* [Build and install on RuneAudio](INSTALL_RUNEAUDIO.md)
* Build and install on Debian-based OS running MPD, follow the instructions
  for [Build and install on Volumio](INSTALL_VOLUMIO.md) but use
  `PLAYER=MPD make` (stretch) or `PLAYER=MPD LDLIBS="-li2c" make` (buster)
  when building mpd_oled


## Credits

C.A.V.A. is a bar spectrum audio visualizer: <https://github.com/karlstav/cava>

OLED interface based on ArduiPI_OLED: <https://github.com/hallard/ArduiPi_OLED>
(which is based on the Adafruit_SSD1306, Adafruit_GFX, and bcm2835 library
code).

C library for Broadcom BCM 2835: <https://www.airspayce.com/mikem/bcm2835/>
