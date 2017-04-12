# SPI

Bei [SPI](http://de.wikipedia.org/wiki/Serial_Peripheral_Interface), Serial-Peripheral-Interface, handelt es sich wie bei I2C um einen seriellen synchronen Bus nach dem [Master/Slave](http://de.wikipedia.org/?title=Master/Slave)-Prinzip. Im Gegensatz zu I2C verfügt SPI über je eine eigene Datenleitung zum Lesen (MISO, Master-In-Slave-Out) bzw. Schreiben (MOSI, Master-Out-Slave-In). Der Empfänger wird durch eine extra Leitung - SS (Slave Select) oder CS (Chip Select) - ausgewählt. Die Geschwindigkeit bei SPI liegt deutlich höher als bei UART und I2C. Für einen Arduino mit 16 MHz Quarz sollte der Takt für den SPI-Bus maximal 4 MHz betragen. Die Übertragung einer Slave-Adresse wie beim I2C-Bus entfällt. Außerdem sind Lesen und Schreiben gleichzeitig möglich. Gängige Anwendungen für SPI sind A/D- und D/A-Wandler sowie EEPROMs. Des Weiteren können auch SD-Karten über SPI angesprochen werden. SPI steht in unzähligen Varianten zur Verfügung, die bekanntesten tragen die Bezeichnung Mode0 bis Mode4. Sie unterscheiden sich in der Art und Weise, wie sich Takt und Daten zueinander verhalten, dass heißt, wann die Daten gültig sind.

Für die Verbindung eines Mikrocontroller mit einem SPI-Gerät sind 5 Leitungen erforderlich, MOSI, MISO, SCK, CS und GND. Jeder weitere Slave benötigt eine weitere CS-Leitung, der Rest wird parallel verdrahtet. Auf dem Bus gibt es jeweils nur eine Verbindung zwischen einem Master und einem Slave, es sind keine gleichzeitigen Verbindungen möglich. 

[SPI-Verbindung](../images/spi-verbindung.png)

Bei der Datenübertragung über SPI gilt, dass jede Übertragung vom Master gesteuert wird, wohingegen der Slave nur auf Anfragen seitens des Masters reagiert. Zunächst zieht der Master die Chip-Select-Leitung (CS-Leitung) für den gewünschten Slave nach +LOW+. Zusammen mit jedem Takt werden dann die Daten über die MOSI-Leitung an den Slave gesendet. Gleichzeitig sendet der angesprochene Slave seine Daten über die MISO-Leitung zum Master.

[SPI-Signale](../images/spi-signal.png)


