# EtherCard for ESP32 - Specifically TTGO T-Display

**EtherCard** is a driver for the ENC28J60 chip, compatible with Arduino IDE.
Adapted and extended from code written by Guido Socher and Pascal Stang.

License: GPLv2

The documentation for this library is at http://jeelabs.net/pub/docs/ethercard/.

ESP_8266 port by Guilherme Poletto.
Based on the work by Seradisis for the STM32 platform.
Available at: https://github.com/Serasidis/STM32duino/tree/master/libraries/Serasidis_EtherCard_STM


<<<<<<< HEAD
## Physical Installation

Custom pins are defined in ethercard.cpp

#define MY_CS       33

#define MY_SCLK     25

#define MY_MISO     27

#define MY_MOSI     26

## Support and credit for original library forked

For questions and help, see the [forums][F] (at JeeLabs.net).
The issue tracker has been moved back to [Github][I] again.

[F]: http://jeelabs.net/projects/cafe/boards
[I]: https://github.com/jcw/ethercard/issues
[S]: https://travis-ci.org/jcw/ethercard.svg
[T]: https://travis-ci.org/jcw/ethercard

## Related Work

There are other Arduino libraries for the ENC28J60 that are worth mentioning:

* [UIPEthernet](https://github.com/ntruchsess/arduino_uip) (Drop in replacement for stock Arduino Ethernet library)
* [EtherShield](https://github.com/thiseldo/EtherShield) (no longer maintained, predecessor to Ethercard)
* [ETHER_28J60](https://github.com/muanis/arduino-projects/tree/master/libraries/ETHER_28J60) (no longer maintained, very low footprint and simple)

Read more about the differences at [this blog post](http://www.tweaking4all.com/hardware/arduino/arduino-enc28j60-ethernet/).
