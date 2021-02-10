# EtherCard

**EtherCard** is a driver for the ENC28J60 chip, compatible with Arduino IDE.
Adapted and extended from code written by Guido Socher and Pascal Stang.

License: GPLv2

The documentation for this library is at http://jeelabs.net/pub/docs/ethercard/.

ESP_8266 port by Guilherme Poletto.
Based on the work by Seradisis for the STM32 platform.
Available at: https://github.com/Serasidis/STM32duino/tree/master/libraries/Serasidis_EtherCard_STM


## Physical Installation

### PIN Connections (using ESP32 with Arduino IDE):

    [ENC]	[ESP32]
    VCC -	3.3V
    GND -	GND
    SO -	MISO [19]
    SI -	MOSI [23]
    SCK -	CLK [18]
    CS -	CSO [5]

### PIN Connections (Using Arduino UNO):

    VCC -   3.3V
    GND -    GND
    SCK - Pin 13
    SO  - Pin 12
    SI  - Pin 11
    CS  - Pin  8 # Selectable with the ether.begin() function

### PIN Connections using an Arduino Mega

    VCC -   3.3V
    GND -    GND
    SCK - Pin 52
    SO  - Pin 50
    SI  - Pin 51
    CS  - Pin 53 # Selectable with the ether.begin() function
    # The default CS pin defaults to 8, so you have to set it on a mega:
    ether.begin(sizeof Ethernet::buffer, mymac, 53)
	
### PIN Connections (using ESP8266 with Arduino IDE):
	
	VCC -	3.3V
	GND -	 GND
	SCK -	GPIO14 == HSPI_CLK	== NodeMcu_D5
	SO	-	GPIO12 == HSPI_MISO == NodeMcu_D6
	SI	-	GPIO13 == HSPI_MOSI == NodeMcu_D7
	CS	-	GPIO15 == HSPI_CS/SS== NodeMcu_D8 !!ATTENTION
			//!!MUST BE LOW FOR THE ESP TO BOOTUP (if high, triggers spi_flash_boot!!)
			//Some ENC28j60 boards have a 10k pullup that MUST be removed
			//as not to interfere with the ESP bootup process



## Original Library Support

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
