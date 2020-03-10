# WordClock-WhiteLEDs

Woordklok met witte LEDs<br>
<img alt="Woordklok" src="woordklokCIMG2963.JPG" width="450" /><br>
De diverse versies Arduino code voor de ATMEGA328-chip gemonteerd op een PCB board bestuurd de 24 LED-strips van de woordklok<br>
Op de PCB kunne de volgende onderdelen worden aangesloten: <br>
- RCT DS3231 ZS-042 clock module<br>
- KY-040 Keyes Rotary Encoder<br>
- LDR light sensor 5528<br>
- Bluetooth RF Transceiver Module HC05<br>
- DCF77 module DCF-2<br>
- FM Stereo Radio Module RDA5807M RRD-102V2.0 <br>
De 74HC595 ULN2803APG combinatie besturen de LED-strips door bits in de 74HC595 te schuiven om de LEDs aan en uit te zetten<br>
Een FT232RL FTDI USB to TTL Serial Module kan gebruikt worden om de ATMEGA te programmeren<br>
De HC05/HM-10 Bluetooth-module wordt gebruikt om de klok te besturen en uit te lezen<br>
Een DCF77-module kan aangesloten worden om de tijd in te stellen via de lange golf<br>
Meer info hier: https://ednieuw.home.xs4all.nl/Woordklok/index.html


