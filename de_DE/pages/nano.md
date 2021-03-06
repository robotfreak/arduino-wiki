# Arduino Nano

Der Arduino Nano ist ein Board im 30-poligen DIL Format. Nesonders geeignet für Steckbrett- und Lochraster Projekte. Es verfügt über die selbe Hardware Ausstattung wie sein großer Bruder, der Arduino Uno. 

![TopView](../images/ArduinoNano_TopView.jpg)
![SideView](../images/ArduinoNano_SideView.jpg)

## Hardware

### Eckdaten 

* Prozessor: 8-Bit RISC ATmega328P mit 32kB Flash (2kB Bootloader), 2kB RAM, 1kB EEPROM
* Versorgungspannung: 5V
* Eingangsspannung: 7-12V empfohlen, 6-20V Limits
* Prozessor Takt: 16MHz
* USB: FT232 beim Original, CH340 Chip beim China Clone, USB Mini Anschluss
* Ein-/Ausgänge: : 14 digitale IO davon 6x PWM, 6 analoge Eingänge (davon 2 alternativ für I2C)
* max Strom pro I/O: 40mA
* Serielle Schnittstellen: I2C, SPI, UART
* Sonstiges: OnBoard LED an Pin13 
* Formfaktor: 30 polig DIL, 45x18mm

### Pinbelegung

![Pinout](../images/Atmega168PinMap2.png) 
Source: Arduino.cc

### Ein- und Ausgänge

* [Seriell (UART)](uart.md): Pin 0 (RX), Pin 1 (TX) Serial1, Serial über USB
* Externe Interrupts: Pin 2, 3 Interrupt auf steigende, fallende oder beide Flanken
* Pulsweitenmodulation PWM: Pin 3,5,6,9,10,11 . 8-Bit PWM 
* [Serial Peripheral Interface (SPI)](spi.md): Pin 10 (SS), 11 (MOSI), 12 (MISO) 13 (SCK)
* [I2C (TWI)](i2c.md): Pin A4 (SDA), A5 (SCL)
* Analoge Eingänge: A0-A7
* AREF: Referenzspannung für analoge Eingänge
* Reset: LOW Signal zum Neustarten des Mikrocontrollers

### Stromversorgung
* USB: 5V Versorgungsspannung über USB Port
* VIN: 6-20V ungeregelte Eingangs Versorgungsspannung
* 5V: geregelte Ausgangs Versorgungsspannung des On-Board Spannungsreglers
* 3.3V: geregelte Ausgangs Versorgungsspannung des On-Board Spannungsreglers. max. 50mA
* GND: Massepegel der Versorgungsspannung 

## Software

## Links

* [Board Beschreibung](https://www.arduino.cc/en/Main/ArduinoBoardNano)
* [Schaltplan](http://download.arduino.org/products/NANO/Arduino%20Nano-Rev3.2-SCH.pdf)






