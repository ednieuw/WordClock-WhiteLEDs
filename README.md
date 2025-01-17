# Word clock white LEDs

Zelfbouw woordklok met witte LEDs.<br>
<img alt="Woordklok" src="woordklokCIMG2963.JPG" width="450" /><br>

### Deze klok heeft sinds 2024 modernere variaties: https://github.com/ednieuw/WordclockSelector

Deze pagina bevat diverse versies Arduino code voor de ATMEGA328 of ATMEGA1284-chip gemonteerd op een PCB board. De code bestuurt de 24 LED-strips van de woordklok.<br>
De originele bouwinstructies staan verderop deze pagina of op de oorspronkelijke pagina hier: https://ednieuw.home.xs4all.nl/Woordklok/index.html

of hier als pdf: https://github.com/ednieuw/Woordklok-witte-LEDs/blob/master/Bouwinstructies%20witlicht%20woordklok.pdf

De volgende onderdelen kunnen worden aangesloten: <br>
- RCT DS3231 ZS-042 clock module<br>
- KY-040 Keyes Rotary Encoder<br>
- LDR light sensor 5528<br>
- Bluetooth RF Transceiver Module HC05/HM10/JDY23<br>
- DCF77 module DCF-2<br>
- FM Stereo Radio Module RDA5807M RRD-102V2.0 <br>
- MAX7219_8DIGIT           // Only with 1284. Not enough pins on ATMEGA328<br>
- DS1820                   // Only with 1284<br>

- ESP32 NTP clock. https://github.com/ednieuw/ESP32SerialNTP-BLE-Clock
  
De 74HC595 ULN2803APG combinatie besturen de LED-strips door bits in de 74HC595 te schuiven om de LEDs aan en uit te zetten<br>
Een FT232RL FTDI USB to TTL Serial Module kan gebruikt worden om de ATMEGA te programmeren<br>
De HC05/HM-10/JDY-23 Bluetooth-modules wordt gebruikt om de klok te besturen en uit te lezen.<br>
Een DCF77-module kan aangesloten worden om de tijd in te stellen via de lange golf<br>
V1.0.0 is een gestripte versie van V112 met alleen functionaliteit voor een draaiknop, DS3231 klokmodule en LDR
Vanaf versie V112 zijn de functionaliteiten met #defines aan of uit te zetten.

<h1 class="auto-style1">Instructie wit licht woordklok</h1>

<img alt="" height="300" src="Bouwpakket_files/zw-klok-CIMG2963.JPG" >

Deze woordklok bestaat uit een matrix van 11 bij 11 letters en wordt verlicht door witte LEDs. 
De woordklok bestaat uit onderdelen zoals in de tabel hieronder is weergegeven. <br>
De woordklokonderdelen zijn voor 23x23cm en 30x30cm woordplaten ontworpen. <br>

Kasten kunnen van diverse soorten hardhout gemaakt worden of van MDF zodat ze in een gewenste kleur te verven zijn.<br>

Dezelfde klok is ook met kleuren-LEDs te maken.https://github.com/ednieuw/Word-Colour-Clock-SK6812-WS2812
of een nog oudere versie hier:(https://ednieuw.home.xs4all.nl/Woordklok/Bouwpakket/Woordklok-Kleur.htm)

Om de tijd via WIFI te ontvangen met deze klok is een instructie <a href="https://github.com/ednieuw/ESP32SerialNTP-BLE-Clock">hier te vinden</a>. <br>
De Bluetooth module wordt dan vervangen door een ESP32-C3 of S3 die via WIFI de tijd ophaalt, een Bluetooth menu en een HTML-pagina voor de bediening van de klok aanmaakt.

De bouwtijd van een klok is 20 - 40 uur. <br>
Het solderen van de printplaat vereist niet veel ervaring en is de moeite waard om zelf te doen. 
	<br>	<br>

![Woordplaat met font mirien](https://github.com/user-attachments/assets/72c445f4-e347-499f-9028-e9c1fb5357e5)
![Woordplaat met font Tomaha ](https://github.com/user-attachments/assets/e9314c45-debd-4e69-8111-75d5b89d1407)
Twee woordplaten met font Mirien en Tahoma

 <h2>Benodigdheden</h2>
<p>Soldeerbenodigdheden<br>
  Multimeter</p>
<table width="730" height="1823" border=1 cellpadding=0 cellspacing=0 class="ms-prof-main">
    <!-- fpstyle: 36,011111100 -->
 <tr>
  <td valign=top class="ms-prof-tl">
  <p>&nbsp;<strong><span class="auto-style1">Onderdelen&nbsp; 
  </span></strong></p>
  </td>
  <td valign=top class="ms-prof-top">
  <p class=auto-style1>&nbsp;</p>
  </td>
  <td valign=top class="auto-style8" style="width: 98px">
  <p class=auto-style1>&nbsp;</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="auto-style6">
  <p class=auto-style7>1 x Kast van hardhout of MDF </p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=88 id="Picture 54" src="Bouwpakket_files/image003.jpg" class="auto-style7"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style7 align=right>€ 80,00</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x Woordplaat 30x30cm Mirien/Thomaha. Vinyl op glas.</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=85 src="Bouwpakket_files/image002.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 70,00</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x Spacerplaat 30x30cm, geschuimd PVC wit 10 MM RAL 
  9003, <strong>zonder</strong> gaten</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=94 height=84 src="Bouwpakket_files/image042.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 20,00</p>
  </td>
 </tr>
 <tr>
   <td valign=top class="auto-style8">
   <strong>PCB met onderdelen</strong></td>
   <td valign=top class="ms-prof-even">&nbsp;
   </td>
   <td valign=top class="auto-style5" style="width: 98px">&nbsp;
   </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x Lege printplaat 10*5 cm</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img alt="PCB" src="Bouwpakket_files/printplaatV26.jpg" width="100" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 15,00</p>
  </td>
 </tr>
    <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x Lege printplaat 10*10 cm</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img alt="PCB" src="Bouwpakket_files/PCBV040-tiny-IMG_0242.JPG" width="66" class="auto-style1" height="55"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 20,00</p>
  </td>
    </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  &nbsp;</td>
  <td valign=top class="ms-prof-even">
  &nbsp;</td>
  <td valign=top class="auto-style5" style="width: 98px">
  &nbsp;</td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>2 x 330Ω weerstand</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=40 src="Bouwpakket_files/image005.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,30</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>3 x 10kΩ weerstand</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=48 src="Bouwpakket_files/image006.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,45</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x 4.7kΩ weerstand</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=38 src="Bouwpakket_files/image007.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,30</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p><span lang=EN-GB class="auto-style1">3 x 74HC595 8-bit shift register DIP16</span></p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=51 src="Bouwpakket_files/image008.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 2,00</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p><span lang=EN-GB class="auto-style1">3 x ULN2803APG voltage regulator DIP18</span></p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=41 src="Bouwpakket_files/image009.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 2,00</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>2 x 10 µF condensator </p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=94 height=20 src="Bouwpakket_files/image011.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,15</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>2 x 22 pF condensator</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=30 src="Bouwpakket_files/image012.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,15</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x 16MHz kristal</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=43 src="Bouwpakket_files/image013.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,50</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x 1N4001 diode</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=29 src="Bouwpakket_files/image014.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,15</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p><span lang=EN-GB class="auto-style1">1 x 78L05/ L7805 voltage regulator</span></p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=29 src="Bouwpakket_files/image015.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,50</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x BC327 transistor</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=94 height=31 src="Bouwpakket_files/image016.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,15</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x BC547 transistor</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=28 src="Bouwpakket_files/image017.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,15</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x LED rood</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=94 height=26 src="Bouwpakket_files/image018.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,15</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x LED geel</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=93 height=24 src="Bouwpakket_files/image019.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,15</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x 28-pins voet voor ATMEGA328 </p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=94 height=31 src="Bouwpakket_files/image020.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 0,50</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x ATMEGA328 processor </p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=94 height=27 src="Bouwpakket_files/image021.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 7,50</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x Dupont-kabel vrouw-vrouw 20-aderig</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=96 height=42 src="Bouwpakket_files/image024.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 3,00</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>2 x pinheader 40 pins haaks&nbsp; </p>
  </td>
  <td valign=top class="ms-prof-even">
  <p>
  <img
  border=0 width=94 height=53 src="Bouwpakket_files/image025.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  € 1,50</td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p><span lang=EN-GB class="auto-style1">1 x&nbsp; KY-040 Keyes Rotary Encoder</span></p>
  </td>
  <td valign=top class="ms-prof-even">
  <p>
  <img
  border=0 width=96 height=56 src="Bouwpakket_files/image026.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  € 2,00</td>
 </tr>
    <tr>
  <td valign=top class="ms-prof-left">
  <p class=auto-style1>1 x RCT DS3231 Precisie klok module ZS-042</p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0
  width=96 height=44 src="Bouwpakket_files/image022.jpg" class="auto-style1"></p>
  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1 align=right>€ 5,00</p>
  </td>
    </tr>
	<tr>
  <td valign=top class="ms-prof-left">
  <p><span lang=EN-GB class="auto-style1">1 x CR 2032 3V lithium batterij</span></p>
  </td>
  <td valign=top class="ms-prof-even">
  <p align=right>
  <img border=0  width=96 height=65 src="Bouwpakket_files/image023.jpg" class="auto-style1"></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1 align=right>€ 3,00</p>  </td>
    </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x lichtsensor </p>  </td>
  <td valign=top class="ms-prof-even">
  <p>
  <img border=0 width=94 height=40 src="Bouwpakket_files/image027.jpg" class="auto-style1"></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class="auto-style1">€ 0,85</p>  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x 22kΩ weerstand</p>  </td>
  <td valign=top class="ms-prof-even">
  <p>  <img border=0 width=93 height=27 src="Bouwpakket_files/image028.jpg" class="auto-style1"></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  € 0,15</td>
 </tr>
 <tr>
   <td valign=top class="auto-style8">   <strong>Voeding en verlichting</strong></td>
   <td valign=top class="ms-prof-even">&nbsp;   </td>
   <td valign=top class="auto-style5" style="width: 98px">&nbsp;   </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x Voeding 12V gelijkstroom, 1,25 Ampere </p>  </td>
  <td valign=top class="ms-prof-even">  <p class=auto-style1>&nbsp;</p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1>€ 10,00</p>  </td>
 </tr>
 <tr>
   <td valign=top class="ms-prof-left"> <p class=auto-style1>1 x Stroom Aansluitkabel Euro-stekker – Kabel, open einde Zwart 1.50 m</p>   </td>
   <td valign=top class="ms-prof-even"> <p class=auto-style1>&nbsp;</p>  </td>
   <td valign=top class="auto-style5" style="width: 98px"> <p class=auto-style1>€ 5,00</p>   </td>
 </tr>
 <tr>
   <td valign=top class="auto-style8">1 x Adapter 12V gelijkstroom, 1 Ampere (dan geen 220V in de klokkast)</td>
   <td valign=top class="ms-prof-even">&nbsp;   </td>
   <td align="right" valign=top class="auto-style7" style="width: 98px">€ 10,00</td>
 </tr>
    <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x 50 cm zwart-rood voedingskabel (0.14 mm2)</p>  </td>
  <td valign=top class="ms-prof-even">  <p class=auto-style1>&nbsp;</p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1>€ 0,20</p>  </td>
    </tr>
 <tr>
<td valign=top class="ms-prof-left">
<table border="0" cellpadding="0" cellspacing="0" width="522">
<colgroup>   <col width="522">   </colgroup>
 <tr height="20">		   <td height="20" width="522" class="auto-style1">		   1 x Female&nbsp; 5.5 x 2.1mm DC Power plug</td>
   </tr>
   </table>
    </td>
   <td valign=top class="ms-prof-even">&nbsp;   </td>
   <td align="right" valign=top style="width: 98px">  <p class=auto-style8 align=right>€ 2,00</p>    </td>
 </tr>
    <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x Verlichtingsgrondplaat 3 x 300 x 300 mm MDF-plaat</p>  </td>
  <td valign=top class="ms-prof-even">  <p class=auto-style1 align=right>&nbsp;</p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1 align=right>€ 3,00</p>  </td>
    </tr>
	<tr>
  <td valign=top class="ms-prof-left">  <p><span lang=EN-GB class="auto-style1">3 x 9-pin Dupont female connector</span></p>  </td>
  <td valign=top class="ms-prof-even"> <p align=right>  <img border=0  width=93 height=58 src="Bouwpakket_files/image010.jpg" class="auto-style1"></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1 align=right>€ 3,00</p>  </td>
    </tr>
 <tr>
  <td valign=top class="ms-prof-left">
  <p><span lang=EN-GB class="auto-style1">1 x 10 m wire wrapping 30 AWG = 0.05 
  mm2 rood</span></p>
  </td>
  <td rowspan=3 valign=top class="ms-prof-even">  <p align=right><span lang=EN-GB class="auto-style1">&nbsp;</span></p>  
 <p><img border=0 width=93 height=19 src="Bouwpakket_files/image029.jpg" class="auto-style1"></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1>€ 2,00</p>  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x 10 m wire wrapping 30 AWG = 0.05 mm2 zwart</p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1>€ 2,00</p>  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x 1 m wire wrapping 30 AWG = 0.05 mm2 geel</p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1>€ 0,20</p>  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>1 x set krimpkous 100 cm x 1.5 mm diam + 10 cm x 5 mm diam</p>  </td>
  <td valign=top class="ms-prof-even">  <p>  <img  border=0 width=94 height=37 src="Bouwpakket_files/image030.jpg" class="auto-style1"></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style1>€ 3,00</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p><span lang=EN-GB class="auto-style1">1 x 2 meter Cool White SMD 2835/3528,   120 LEDS/meter, LED-strip 12V</span></p>  </td>
  <td valign=top class="ms-prof-even">  <p>  <img  border=0 width=93 height=20 src="Bouwpakket_files/image031.jpg" class="auto-style1"></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">  <p class=auto-style1>€ 15,00</p>  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1>&nbsp;</p>  </td>
  <td valign=top class="ms-prof-even">  <p class=auto-style1>&nbsp;</p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style5>&nbsp;</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  &nbsp;</td>
  <td valign=top class="ms-prof-even">  &nbsp;</td>
  <td valign=top class="auto-style5" style="width: 98px">  &nbsp;</td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p class=auto-style1><strong>Optioneel</strong></p>  </td>
  <td valign=top class="ms-prof-even">  <p class=auto-style1>&nbsp;</p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  <p class=auto-style5>&nbsp;</p>
  </td>
 </tr>
 <tr>
  <td valign=top class="ms-prof-left">  <p><span lang=EN-GB class="auto-style1">FT232RL 5.5V FTDI USB to TTL Serial   Module + 0.1uF+10 k</span><span class="auto-style1">Ω</span></p>  </td>
  <td valign=top class="ms-prof-even">  <p align=right><span  lang=EN-GB class="auto-style1">&nbsp;</span></p>  </td>
  <td valign=top class="auto-style5" style="width: 98px">
  € 15,00</td>
 </tr>
 <tr>
   <td valign=top class="ms-prof-left"><span lang=EN-GB class="auto-style1">   Wireless Serial 6 Pin Bluetooth RF Transceiver Module HC05 (Android, W10)</span></td>
   <td valign=top class="ms-prof-even">&nbsp;   </td>
   <td valign=top class="auto-style5" style="width: 98px"><div align="right" class="auto-style1">   € 10,00</div></td>
 </tr>
 <tr>
   <td valign=top class="ms-prof-left"><span lang=EN-GB class="auto-style1">
   Wireless Serial 6 Pin Bluetooth RF Transceiver Module H</span><span class="auto-style1">M10</span><span lang=EN-GB class="auto-style1"> 
   (</span><span class="auto-style1">Android, Apple IOS</span><span lang=EN-GB class="auto-style1">)</span></td>
   <td valign=top class="ms-prof-even">&nbsp;
   </td>
   <td valign=top class="auto-style5" style="width: 98px">€ 10,00</td>
 </tr>
 <tr>
   <td valign=top class="auto-style8">DCF77 DCF-2 module</td>
   <td align="center" valign=middle class="ms-prof-even">
   <img src="Bouwpakket_files/DCF-2.jpg" width="92" height="71" class="auto-style1"></td>
   <td valign=top class="auto-style5" style="width: 98px"><div align="right" class="auto-style1">
	   € 20,00</div></td>
 </tr>
 </table>

<p class=auto-style2>
<img alt="PCB-V40" height="600" src="Bouwpakket_files/WoordklokV40.jpg" width="600"></p>
<p class=auto-style2>Nieuwe uitvoering printplaat met plek om de modules zonder 
draden aan te sluiten. Deze printplaat is 10*10 cm.<br></p>
<p class=auto-style2>Hoe werkt de printplaat:</p>

<p class=auto-style1>De Arduino-software (<a href="../Versions/Softwareversions.html">Sourcecode 
van de software</a> of <a href="https://github.com/ednieuw/WordClock-WhiteLEDs">
Github</a>) stuurt een 24-bits code naar de drie 74HC595 8-bit shiftregisterchips via pin 10. Pin 11 en 12 dienen om 
de 74HC595-chip te synchroniseren. </p>

<p class=auto-style1>Pin 9 stuurt de gele LED aan en pin 13 de rode LED.</p>

<p class=auto-style1>Aan de andere zijde van de 74HC595-chip zal bij een 
gestuurde 1-bit een 5V spanning staan en bij een gestuurde 0-bit 0V. Omdat de spanning van 5V te 
laag is om de licht-LED’s, die achter de woorden zitten, aan te sturen zijn de 
ULN2803APG voltage regulator chips geplaatst. De transistoren in deze chip zorgen ervoor 
dat het 5V-signaal in een 12V 
voedingsspanning voor de LED wordt . Deze chips zijn krachtig genoeg om voldoende stroom te leveren om de licht-LED’s 
te laten branden.</p>

<p class=auto-style1>De licht-LED’s geven te veel licht als het donker wordt en 
moeten gedimd worden. Dat kan met een gloeilamp door de spanning te verlagen 
maar bij LED’s werkt dat in een beperkt spanningsgebied. De truc is om de stroom 
te pulsen. Dus de LED’s meerdere keren per seconden aan en uit te zetten. Als je 
dan met een frequentie van meer dan 50Hz doet dan ziet ons oog dat niet. Hoe 
lichter het moet zijn hoe langer de aan-puls. De lichtsensor (LDR) meet de 
lichtintensiteit en dit analoge signaal komt binnen op pin A2. De software 
berekent de lengte van de puls en stuur het pulsesignaal naar pin 5. De twee 
diodes BC547 en BC327 maken van dit 5V signaal een 12V signaal dat via een diode 
op de pluspool van de licht-LED’s wordt gezet.</p>

<p class=auto-style1>De RST, RX en TX poort van de Arduino-chip kunnen worden 
gebruikt om software te laden in de chip maar wordt ook gebruikt om diverse meetwaarden uit te lezen 
zoals de lichtsensor. <br>Hiervoor is een zogenaamde “FT232RL 3.3V 5.5V FTDI USB to 
TTL Serial Adapter Module” nodig. <br>Samen met een weerstand en 
een condensator kan deze op de RST, RX en TX pinnen worden aangesloten. <br>Je kan 
ook de ATMEGA 328-chip een Arduino UNO zetten en dan 
programmeren. </p>

<p class=auto-style1>Het kristal in metalen huis met 16000 daarop geprint is het hart van de processor en geeft de processor opdracht om 16 miljoen keer per seconde een processtap uit te 
voeren.</p>

<p class=auto-style1>De 10 uF-condensatoren zorgen er voor dat stroomrimpels gedempt 
worden.&nbsp;</p>

<p>
<img
border=0 width=616 height=306 src="Bouwpakket_files/image032.jpg" class="auto-style1"><span class="auto-style1">&nbsp;<br>&nbsp;&nbsp;</span></p>
<p>
&nbsp;</p>

<p class=auto-style2><strong>De printplaat solderen</strong></p>

<p class=auto-style1>Op de printplaat staat aangegeven waar de diverse 
onderdelen gesoldeerd moeten worden.<br>Let op de inkepingen aangegeven op de IC’s en printplaat!<br>
De 330 ohm weerstanden bij de LEDs mogen ook 470Ω of hoger zijn.</p>

<p class=auto-style1>Als alles op zijn plek gesoldeerd is meet dan of de 
printplaat geen kortsluiting heeft.</p>

<p class=auto-style1>De weerstand gemeten tussen 5V en GND is hoger dan 5kΩ. De weerstand tussen 
12V en GND is ook meer dan 5kΩ. <span class="auto-style1"><br>De weerstand loopt langzaam op tijdens het meten 
omdat de 10 µF condensatoren door de meting met de multimeter vol raken.<br></span><br class="auto-style1">
<span class="auto-style2">Vergeet niet</span><span class="auto-style1"> een draad 
vanuit het midden van de printplaat, bij de schuin geplaatste weerstand, aan P5 
te solderen.<br>&nbsp;</span>&nbsp;&nbsp;</p>

<p>
<img
border=0 width=383 height=209 src="Bouwpakket_files/image033.jpg" class="auto-style1">&nbsp;</p>

<p>
<img border=0 width=386 height=289
src="Bouwpakket_files/image034.jpg" alt=CIMG1679 class="auto-style1"></p>

<p class=auto-style1>Breek de haakse pinheaders op lengte met behulp van een 
puntbektang en soldeer ze aan de printplaat. </p>

<p>
<img
border=0 width=398 height=179 src="Bouwpakket_files/image035.jpg" class="auto-style1"></p>

<p class=auto-style1>Plaats de ATMEGA 328-processor in de voet. Let op de 
inkeping!</p>
<p class=auto-style1>De laatste stabiele <a href="https://github.com/ednieuw/WordClock-WhiteLEDs/blob/master/Character_Clock_V108_328-1284.ino">
softwareversie is V108</a>. Deze ondersteund de rotary encoder draaiknop, 
Bluetooth en de DCF-ontvanger</p>
	<span class="auto-style1">Onderin deze pagina of op <a href="https://github.com/ednieuw/WordClock-WhiteLEDs">Github</a> zijn hyperlinks naar andere 
	stabiele versies te vinden</span><b>.<br
clear=all class="auto-style1">
	</b>

<p class=auto-style2>De lichtsensor</p>

<p>
<img
border=0 width=291 height=163 src="Bouwpakket_files/image036.jpg" class="auto-style1">&nbsp;</p>

<p class=auto-style1>Knip drie draden van 20-30 cm.</p>

<p class=auto-style1>Schuif eerst de krimpkousen aan de poten van de LDR.</p>

<p class=auto-style1>Soldeer de lichtsensor en de 22kΩ weerstand zoals 
aangegeven in de foto.</p>

<p class=auto-style1>Soldeer de gele draad aan de connector die gelabeld wordt 
met A2</p>

<p class=auto-style1>Soldeer de zwarte draad aan de aarde.</p>

<p class=auto-style1>Soldeer de rode draad aan 5V.</p>

<p class=auto-style1>Monteer alle open verbindingen af met krimpkous en krimp ze 
met hete lucht.</p>

<p class=auto-style1>Label de aansluitingen met een sticker.</p>

<p>
<img
border=0 width=369 height=181 src="Bouwpakket_files/image037.jpg" class="auto-style1">&nbsp;</p>

<p>
<img
border=0 width=368 height=199 src="Bouwpakket_files/image038.jpg" class="auto-style1"><br></p>

<p class=auto-style2>De draaiknop (Rotary encoder KY-040)</p>

<p class=auto-style1>Verbind de 5 vrouw-vrouw Dupont-kabels recht door.</p>

<p class=auto-style1>CLK naar P8 (Voor de softwareversie V080 was dit P2)</p>

<p class=auto-style1>DT naar P3</p>

<p class=auto-style1>SW naar P4</p>

<p class=auto-style1>Plak deze drie aansluitingen met een stikker bij elkaar</p>

<p class=auto-style1>+ naar 5V</p>

<p class=auto-style1>GND naar GND</p>

<p class=auto-style1>Plak deze twee aansluitingen met een stikker bij elkaar</p>

<p class=auto-style1>Label de aansluitingen.</p>
<p>
<img
border=0 width=495 height=147 src="Bouwpakket_files/image039.jpg" class="auto-style1">&nbsp;</p>

<p class=auto-style2>De klok</p>

<p class=auto-style1>Verbind de 4 vrouw-vrouw Dupont-kabels recht door.</p>

<p><span lang=EN-GB class="auto-style1">SCL naar A5.</span></p>

<p><span lang=EN-GB class="auto-style1">SDA naar A4.</span></p>

<p class=auto-style1>Plak deze drie aansluitingen met een stikker bij elkaar.&nbsp;</p>

<p class=auto-style1>VCC naar 5V.</p>

<p class=auto-style1>GND naar GND.</p>

<p class=auto-style1>Plak deze drie aansluitingen met een stikker bij elkaar.</p>

<p class=auto-style1>Label de aansluitingen.&nbsp;</p>

<p class=auto-style2>De voeding</p>

<p class=auto-style1>Maak het koper vrij aan de vier uiteinden van de twee-aderige 
draad en breng soldeer aan. </p>

<p class=auto-style1>Sluit de 12V-voeding aan op de 12V-aansluiting rechts 
bovenin de printplaat.<br>NB. Je kan ook een USB 5V naar 12V kabel gebruiken om 
de klok te voeden. Dan kan met een simpele telefoonvoeding de klok gevoed 
worden.</p>

<p class=auto-style1>Dat kan door middel van een Dupont-kabelstekkers of direct 
aan de printplaat gesoldeerd.</p>

<p>
<img
border=0 width=398 height=300 src="Bouwpakket_files/image040.jpg" alt=CIMG1719 class="auto-style1">&nbsp;</p>

<p><span class="auto-style2">De grondplaat met</span> <span class="auto-style2">
verlichting</span></p>

<p class=auto-style1>Plak een wit vel A4 op de grondplaat waar de LED-verlichting 
op wordt geplakt. </p>

<p class=auto-style1>&nbsp;</p>

<p>
<img
border=0 width=343 height=271 src="Bouwpakket_files/image041.jpg" class="auto-style1"></p>

<p class=auto-style1>Gebruik de spacerplaat om de kaders met een potlood op de 
template aan te geven.</p>

<p>
<img
border=0 width=345 height=258 src="Bouwpakket_files/image042.jpg" class="auto-style1"></p>

<p class=auto-style1>Je kunt de LED-strip knippen per drie LED’s. De knipplaats 
is duidelijk op de strip aangegeven. </p>

<p>
<img
border=0 width=491 height=116 src="Bouwpakket_files/image043.jpg" class="auto-style1"></p>

<p class=auto-style1>Plak het volgende aantal stukjes 3-LED-strips over de tekst 
van het sjabloon.</p>

<p class=auto-style1>Let er op dat de plus steeds aan de bovenkant van de 
geplakte strip zit</p>

<table border=0 cellspacing=0 cellpadding=0 align=left>
 <tr>
  <td width=77>
  <p class=auto-style1>&nbsp;</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>30 cm</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>23 cm</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>HET</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>2</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>IS</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>1</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>1</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>WAS</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>2</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>VIJF</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>TIEN</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>KWART</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>4</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>3</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>VOOR</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>OVER</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>PRECIES</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>5</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>4</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>HALF</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>ELF</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>2</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>VIJF</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>TWEE</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>EEN</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>2</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>VIER</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>TIEN</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>TWAALF</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>4</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>3</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>DRIE</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>NEGEN</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>4</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>3</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>ACHT</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>3</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>ZES</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>2</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>ZEVEN</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>4</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>3</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>UUR</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>2</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>2</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>RESERVE</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>5</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>5</p>
  </td>
 </tr>
 <tr>
  <td width=77>
  <p class=auto-style1>Totaal</p>
  </td>
  <td width=62>
  <p class=auto-style1 align=center>72</p>
  </td>
  <td width=66>
  <p class=auto-style1 align=center>56</p>
  </td>
 </tr>
</table>

<p><br
clear=all class="auto-style1">
</p>

<p class=auto-style1>Knip een benodigde lengte af en soldeer een rode en een 
zwarte wire-wrapdraad. </p>

<p class=auto-style1>Plak de LED-strips op de verlichtingsgrondplaat en zorg dat 
de plusaansluiting aan de bovenkant zit.</p>

<p class=auto-style1>&nbsp;</p>

<p class=auto-style1>In de woorden PRECIES en TWAALF passen de LEDs passen niet 
over de hele breedte.&nbsp;&nbsp; <br>Knip de LED-strip in 
twee stukken en verdeel deze. Zie foto.<br>Soldeer de LEDS-strips onderling weer vast met een draad. </p>

<p class=auto-style1>Boor gaten van 2 mm naast de aansluitingen van de LED-strip. </p>

<p class=auto-style1>Nummer de aansluitingen op de achterkant 1 t/m 23. 1 = HET, 
2=IS, ect, 23 = UUR. <br>Nummer 24 is reserve.</p>

<p class=auto-style1>Deze nummering gebruik je straks om de draden aan de juiste 
aansluiting te solderen.</p>
	<p>
<img
border=0 width=492 height=264 src="Bouwpakket_files/image044.jpg"
alt=Kloklichten class="auto-style1"></p>

<p class=auto-style1>Breng soldeer aan op de LED-stripaansluiting en soldeer 
later de draad erin. </p>

<p class=auto-style1>Rode draad aan plus, zwarte draad aan de min.</p>

<p class=auto-style1>Controleer of de LED’s branden met een 9V batterij. </p>

<p>
<img
border=0 width=417 height=302 src="Bouwpakket_files/image045.jpg"
alt=Kloklichten-afmaken class="auto-style1"></p>

<p class=auto-style1>Stikker drie&nbsp; 9-pins Dupont-vrouw aansluitstekkers als op 
de foto.</p>

<p class=auto-style1>Met de draden naar rechts, stekker links </p>

<table border=0 cellspacing=0 cellpadding=0>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>8</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>16</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>24</p>
  </td>
  <td>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>7</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>15</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>23</p>
  </td>
  <td>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>6</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>14</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>22</p>
  </td>
  <td valign=top>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>5</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>13</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>21</p>
  </td>
  <td valign=top>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>4</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>12</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>20</p>
  </td>
  <td valign=top>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>3</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>11</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>19</p>
  </td>
  <td valign=top>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>2</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>10</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>18</p>
  </td>
  <td valign=top>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>1</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>9</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>17</p>
  </td>
  <td valign=top>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
 <tr>
  <td style="width: 39px">
  <p class=auto-style1>+</p>
  </td>
  <td style="width: 40px">
  <p class=auto-style1>+</p>
  </td>
  <td style="width: 37px">
  <p class=auto-style1>+</p>
  </td>
  <td valign=top>
  <p class=auto-style1>------------</p>
  </td>
 </tr>
</table>

<p class=auto-style1>Controleer de nummering van de stekkers met die op de 
printplaat.</p>

<p class=auto-style1>Bundel de rode draden van de eerste acht LED-strips en 
soldeer ze aan elkaar.</p>

<p class=auto-style1>Schuif er een krimpkous overheen en soldeer de + draad van 
de 9-pins Dupont-vrouw aansluitstekker vast</p>

<p class=auto-style1>Krimp de kous met hete lucht of de soldeerbout vast.&nbsp;</p>

<p class=auto-style1>Schuif een cm 1.5mm krimpkous over de draden van de 
aansluitstekker.</p>

<p class=auto-style1>Sluit de zwarte draad van LED-strip 1 aan op aansluiting 1 
van de 9-pins Dupont-vrouw aansluitstekker. </p>

<p class=auto-style1>Krimp de krimpkous met hete lucht of de soldeerbout.&nbsp;</p>

<p class=auto-style1>Herhaal dit voor alle drie de stekkers en 23 aansluitingen. </p>

<p class=auto-style1>Aansluiting 24 is een reserve-aansluiting. Soldeer er een 
stukje LED-strip aan vast en laat die in de kast als reserve LED’s.&nbsp;</p>

<p class=auto-style2>De klok in elkaar zetten</p>

<p class=auto-style1>Het is handig om de onderdelen van de klok met papier 
afplakband vast te plakken. Dit plakband komt makkelijk los. </p>

<p class=auto-style1>Plat de verlichtingsplaat en spacer aan elkaar vast. </p>

<p class=auto-style1>Plak over de spacer een wit vel papier. Bij een 30x30 cm 
klok is een A3-vel nodig of twee aan elkaar geplakte A4-tjes. Zorg en dan voor 
dat het plakbank niet door de letters te zien is. Het papier geeft een mooie 
tekening aan de verlichte letters. Gebruikt niet te goedkoop papier. Mogelijk 
dat dit op de duur verkleurd.</p>

<p class=auto-style1>Leg de woordplaat over het papier en fixeer deze ook met 
plakband. </p>

<p class=auto-style1>Bij een hardhouten klok wordt, afhankelijk van de 
uitvoering, de woordplaat in de sleuf in de kast geschoven. Monteer daarna de 
vierde, onderkant van de kast. Verlijm dit of plak het met plakbank tijdelijk 
vast. Zie: “Ontwerp kast 30 cm-klok”.</p>

<p class=auto-style1>Als alles goed gelabeld is kunnen de klok, rotary encoder, 
LDR, voeding aangesloten worden.</p>

<p class=auto-style1>Monteer de kast af.&nbsp;</p>
<table style="width: 920px">
</table>

<p>
<img
border=0 width=602 height=452 src="Bouwpakket_files/image046.jpg" class="auto-style1"></p>

<p class=auto-style1>Als alles goed is gegaan ziet de binnenkant er ongeveer zo 
uit.<br>
<span class="auto-style9">NB De uitvoering op defoto is een hardhouten kast van 
30x30 cm en drukknoppen in plaats van een rotary encoder.</span></p>

<p class=auto-style2><strong>FTDI-board aanpassen om de klok te programmeren en de 
seriële poort uit te lezen.</strong></p>

<p class=auto-style1>Met een FTDI-board kan de ATMEGA328-chip verbonden worden 
met de Arduino programmeersoftware op de PC. </p>

<p class=auto-style1>De software in de klok geeft informatie, zoals de tijd, 
door naar de PC via deze verbinding maar de ATMEGA328 kan zo ook geprogrammeerd 
worden. Om het geheel te laten werken moet de FT232RL 5.5V FTDI USB to TTL 
Serial Module aangepast worden. </p>

<p class=auto-style1>Een 100 nF condensator wordt tussen de DTR-pin van de FTDI 
en de RST-pin van het klokboard gesoldeerd. Een 10 kΩ weerstand wordt tussen 5V 
en de RST-pin van het klokboard gesoldeerd.<br><span class="auto-style9">Deze 
schakeling is nodig om software in de ATMEGA328 te kunnen laden. In de ATMEGA328 
zit een programma (een bootloader) dat start en heel kort wacht op een programma 
dat in de chip moet worden gezet . Komt dat programma niet dan start het 
klokprogramma op. Met de DTR-pin wordt de chip gereset zodat de bootloader 
start. De Arduino IDE-software op de PC zorgt voor deze aansturing als een 
programma "geupload" wordt.<br></span></p>

<p>
<img
border=0 width=424 height=151 src="Bouwpakket_files/image047.png" class="auto-style1"></p>

<p class=auto-style1>Let op dat TX en RX gekruist worden. TX aan RX en RX aan 
TX.</p>

<p><span class="auto-style3">Laat de USB-stekker niet in de computer zitten als 
de klok op 220V draait en de computer uitgezet wordt.</span><span class="auto-style1"> 
<br>Er loopt dan stroom van de klok naar de PC met als resultaat dat onderdelen op 
de printplaat defect raken. <br>Een diode op de 5V aansluiting voorkomt deze storing 
niet. <br>Mogelijk moet er tussen TX- en RX-datalijnen ook nog een diode geplaatst worden.<br>
NB Ik heb printplaatjes om de FTDI makkelijker te monteren. <br></span></p>
<p>
<img alt="PCB-V40 woordklok" height="450" src="Bouwpakket_files/PCB-V40-IMG_0242.JPG" width="450"></p>
<p>Met de 10 x 10 cm PCB kunnen de onderdelen en modules een stuk netter 
gemonteerd worden.<br>Van boven naar onder de RTC, lege aansluitplek, LDR 
aansluiting, FTDI en Bluetooth module.</p>

<p class=auto-style2><strong>Bluetooth-verbinding</strong></p>

<p class=auto-style1>Met de <a>
Bluetooth-module</a> kan er een Bluetooth-verbinding met de klok gemaakt 
worden.</p>

<p class=auto-style1>In onderstaande hoofdstuk staat beschreven aan welke pins 
de module aangesloten en hoe de naam van de module aangepast wordt.<br>Met een Bluetooth-terminal app op de telefoon kan de tijd 
als hhmmss of hhmm naar de klok gestuurd worden.</p>

<p class=auto-style1>De klok stuurt elke halve minuut gegevens, naar de terminal app 
terug. <br>Voor Android en Iphone zijn Bluetooth terminal apps te 
vinden. <br>Bluetooth terminalprogramma’s zijn ook voor PC’s te vinden.<br>
<img alt="Terminal" height="450" src="Bouwpakket_files/Phone-BT-WP_20160107.jpg" width="450"></p>

<p class=auto-style1><strong>Aansluiting van een Bluetooth-module aan de klok</strong></p>

<p class=auto-style1>De Bluetooth-module communiceert tussen RX en TX met 3.3V. <br>
Het is mogelijk om de module direct op de 5V Arduino-poorten aan te sluiten maar 
het verlengt de levensduur van de module als de spanning naar 3.3V wordt 
verlaagd. </p>

<p><span class="auto-style1">Dit kan met een 3.3V-5V TTL Level Logic Level 
Converter module, of met een “voltage divider”-schakeling zoals hieronder 
weergegeven.</span><br class="auto-style1">
<span class="auto-style1">Je kan de weerstanden in de bedrading</span><span lang=NL class="auto-style1"> </span>
<span class="auto-style1">van de module naar de printplaat monteren.<br><br>In de 
software is de Bluetooth-module op pin 6 en 7 aangesloten.<br>
<span class="auto-style9">BT_RX = 6, // Bluetooth RX connect to TXD op de BT 
module</span><br class="auto-style9"><span class="auto-style9">BT_TX = 7, // 
Bluetooth TX connect to RXD op de BT module</span><br><br>Verbind <br>- VCC aan 
5V<br>- 
	GND aan GND<br>- pin 6 aan de TXD van de Bluetooth-module<br>- pin 7 aan de RXD van de Bluetooth-module</span></p>

<p>
<img
border=0 width=616 height=190 src="Bouwpakket_files/Bluetooth3_3V.jpg"
alt="Bluetooth naar 3.3V" class="auto-style1"></p>

<p class=auto-style1>C<strong>ommuniceren via Bluetooth met de HM10 BLE voor 
Apple IOS en Android</strong></p>
	<p><span class="auto-style1">Met de HM10 BLE module kan draadloos 
	gecommuniceerd worden met Apple IOS en Android.</span><br class="auto-style1">
    <span class="auto-style1">Er moet dan wel met het programma BLE scanner (App 
	store) contact worden gemaakt. Dit programma zorgt dat het HM10 
	communicatieprotocol geinstalleerd is. (Of je dit programma echt nodig hebt 
	is mij onduidelijk. Mogelijk dat nieuwere versies van de telefoon dit niet 
	meer nodig heeft)</span><br class="auto-style1">
    <span class="auto-style1">Met BLE scanner kan de HM10-module "Connect" 
	worden.</span></p>
	<p><span class="auto-style1">Daarna kan met een serial terminal programma (Voor 
	IOS "HM10 Bluetooth serial light"-app van Alex van der Lugt of "BLE Terminal 
	HM-10")&nbsp;commando's worden overgestuurd en de klokuitvoer opgevangen 
	worden.
	<br>Voor Android kan het programma BLE scanner van Blue Pixel Technologies 
	LLP geinstalleerd worden.<br>Serial Bluetooth Terminal van Kai Morich werkt 
	goed als terminal.</span><br class="auto-style1">
  <img src="Bouwpakket_files/IOSBluetooth.jpg" width="450" class="auto-style1"><span class="auto-style1"><img alt="android" height="245" src="Bouwpakket_files/KaiMorich.jpg" width="259">
	</span> </p>
	<p><span class="auto-style1">Connect met BLE scanner of met de serial 
	terminal programma (heb geduld, het kan wel 5 minuten duren voordat je de 
	naam van de module te zien krijgt).<br>Gebruik het Serial Bluetooth Terminal 
	voor de communicatie. <br>Als de i van Info wordt ingetikt verschijnt het 
	menu in het terminalprogrammavenster</span></p>
	<p><span class="auto-style10">"Woordklok nov 2019",</span><br class="auto-style10">
	<span class="auto-style10">"Enter time as: hhmm (1321) or hhmmss (132145)",</span><br class="auto-style10">
	<span class="auto-style10">"Enter A for normal display",</span><br class="auto-style10">
	<span class="auto-style10">"Enter B to suspress Het Is Was in display",</span><br class="auto-style10">
	<span class="auto-style10">"Enter C to suspress Het Is Was after 10 
	seconds",</span><br class="auto-style10"><span class="auto-style10">"Enter D 
	D15122017 for date 15 December 2017",</span><br class="auto-style10">
	<span class="auto-style10">"Enter G for DCF-signal info on display",</span><br class="auto-style10">
	<span class="auto-style10">"Enter Mnn (M90)Max light intensity (1% - 250%)",</span><br class="auto-style10">
	<span class="auto-style10">"Enter Lnn (L5) Min light intensity ( 1 - 255)",</span><br class="auto-style10">
	<span class="auto-style10">"Enter I for info",</span><br class="auto-style10">
	<span class="auto-style10">"Enter X for Demo mode",</span><br class="auto-style10">
	<span class="auto-style10">"Enter Z for Self test",</span><br class="auto-style10">
	<span class="auto-style10">"Ed Nieuwenhuys V108 September 2019" };</span></p>
	<p class="auto-style1">Met A, B of C als commando kan HET IS WAS aan of uit 
	worden gezet. C laat HET IS WAS 10 seconden zien.<br>Met D kan de datum 
	gecorrigeerd worden. Voor de werking van de tijd in de klok heeft dit geen 
	effect<br>Met G kan het ontvangen DCF-signaal aan de voorkant van de klok in 
	de woorden HET IS WAS gevolgd worden.<br><span class="auto-style9">De DCF-ontvangst 
	die bij goede ontvangst regelmatig eens per seconde knippert is ook te zien 
	in de LED op de printplaat maar dat in bij een dichte kast lastig te zien.<br>
	</span>Met Mnnn, waarin n een getal tussen 0 en 250 is, kan de sterkt van de 
	LED's aangepast worden. <br><span class="auto-style9">Normaal is 60-80 als 
	de LDR goed geplaatst is.</span> <br>Met Lnnn kan de laagste lichtsterkte 
	ingesteld worden. <br><span class="auto-style9">Als de LDR nog nauwelijks 
	signaal ontvangt zijn de ontvangen waarden 0, 1, 2 et cetera. Dit 
	veroorzaakt gespring in lichtsterkte. L5 is een mooie ondergrens.</span><br>
	Met I wordt het menu getoond.<br>X&nbsp; is de demo-mode<br>Invoer van Z 
	start een zelftest om de werking van de LED's te controleren</p>

	<p><span class="auto-style1"><strong>De naam aanpassen van de Bluetooth 
	module HM10 BLE</strong> 
	</span> </p>
	<p><span class="auto-style1">Gekoppeld via een FTDI kan in de Arduino IDE 
	met "Serial monitor" aan de Bluetooth-module AT commandos gegeven worden. 
	</span> <br class="auto-style1">
	</p>
	<p><span class="auto-style1">Verbind de 5V en GND met elkaar en RX aan TX en 
	TX aan RX. </span> </p>
	<p><span class="auto-style1">Verbind de FTDI aan de USB-poort van de PC.<br></span><br class="auto-style1">
	<span class="auto-style1">Start de Arduino-console en kies de COM-poort Bij 
	Tools in het menu. Start de Serial monitor (Icoon lijkend op een 
	vergrootglas, Onder het X rechts boven).<br></span><br class="auto-style1">
	<span class="auto-style1">Tik AT en return. Je ziet OK in het scherm 
	verschijnen.<br></span><br class="auto-style1">
      <span class="auto-style1">Zie vorige paragraaf voor AT commando's.<br></span><br class="auto-style1">
        <span class="auto-style1">
        AT+NAMEnieuwenaam geeft de module de naam: nieuwenaam 
	</span> </p>
	<p>
	<img alt="HM10 met FTDI" src="Bouwpakket_files/HM10-FTDI.jpg" width="450" class="auto-style1"></p>

<p class=auto-style1><strong>De naam aanpassen van de Bluetooth module 
HC-05/ZS-040</strong></p>

<p class=auto-style1>Met een Android-telefoon kan een HC-05 Bluetooth-module nog 
gebruikt worden. Deze modules zijn vaak erg goedkoop<br>De naam waaronder je de module in de telefoon kan vinden is 
HC05 of iets dergelijks. <br>Om de module een beter herkenbare naam te laten 
uitzenden kan de naam worden anagepast.<br>De Bluetooth-module dient hiervoor 
aan een Arduino te worden gekoppeld en in programmerstand te worden gezet.<br>
dit gaat als volgt:</p>
	<p class=auto-style1>- Verbind VCC en GND, pin 6 aan de TXD en pin 7 aan RXD 
	van de Bluetooth-module.</p>

<p class=auto-style1>- Laad de volgende sketch om tussen de Arduino en de 
Bluetoothmodule te kunnen communiceren en de naam te veranderen.<span lang=EN-GB class="auto-style1"><br>
-------------------------</span></p>
	<ol>
		<li><span lang=EN-GB class="auto-style1">#include &lt;SoftwareSerial.h&gt;</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;SoftwareSerial BTSerial(6, 7); 
		// RX | TX</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;void setup()</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;</span><span class="auto-style1">{</span></li>
		<li><span class="auto-style1">&nbsp;&nbsp;
</span><span lang=EN-GB class="auto-style1">pinMode(9, OUTPUT);&nbsp; // this pin 
		will pull the HC-05 pin 34 (key pin) HIGH to switch module to AT mode</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; digitalWrite(9, HIGH);</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; Serial.begin(9600);</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; Serial.println("Enter AT 
		commands:");</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; BTSerial.begin(38400);&nbsp; // 
		HC-05 default speed in AT command more</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;}</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;void loop()</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;{</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; // Keep reading from HC-05 
		and send to Arduino Serial Monitor</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; if (BTSerial.available())</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp;&nbsp;&nbsp; Serial.write(BTSerial.read());</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; // Keep reading from Arduino 
		Serial Monitor and send to HC-05</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp; if (Serial.available())</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;&nbsp;&nbsp;&nbsp; BTSerial.write(Serial.read());</span></li>
		<li><span lang=EN-GB class="auto-style1">&nbsp;</span><span class="auto-style1">}</span></li>
	</ol>
	<p class=auto-style1>---------------------------------</p>

<p class=auto-style1>- Ontkoppel de Arduino van de USB-kabel zodat de Arduino en 
Bluetoothmodule spanningsloos zijn geworden.</p>

<p class=auto-style1>- Leg een draadje tussen de 5V van de Arduino en pin 34. (rechtsboven 
in de Bluetooth-module als de pinnen naar beneden wijzen. Zie foto).</p>

<p class=auto-style1>- Sluit de Arduino weer op de PC aan en open de serial 
monitor in de Arduino software. (icoon rechtsboven onder X (kruisje)).</p>

<p class=auto-style1>- De rode LED op de Bluetooth-module gaat nu langzaam 2 sec 
aan, 2 sec uit, knipperen.</p>

<p><span class="auto-style1">- </span>
<span lang=EN-GB class="auto-style1">Tik in:<br></span>
<span class="auto-style1">----------------</span><span lang=EN-GB class="auto-style1"><br>
AT </span><span class="auto-style1">--&gt; Dit geeft </span><span lang=EN-GB class="auto-style1">
&nbsp;OK </span>
<span class="auto-style1">&nbsp;terug</span><span lang=EN-GB class="auto-style1"><br>
AT+NAME=KLOK<br>AT+RESET&nbsp;<br></span>------------------<span lang=EN-GB class="auto-style1"><br>
De</span><span class="auto-style1"> de</span><span lang=EN-GB class="auto-style1">fault 
passkey = 1234<br>--------------------------</span></p>

<p><span lang=EN-GB class="auto-style1">Here is an important note, if the key 
pin is not high, i.e. not connected to V</span><span class="auto-style1">CC</span><span lang=EN-GB class="auto-style1"> while receiving AT commands(if you 
did not solder the wire and released it after the module entered AT mode), it 
will not show the default name even after giving right command. But you can 
still change the name by the command mentioned above. To verify if the name has 
really changed, search the device from your pc/mobile. The changed name will 
appear. To change baud rate, type AT+UART=desired baud rate. Exit by sending 
AT+RESET command.</span></p>

<p><span lang=EN-GB class="auto-style1">Most useful AT commands are</span><span class="auto-style1">:</span><span lang=EN-GB class="auto-style1"><br>
AT : Check the connection.<br>AT+NAME : See default name<br>AT+ADDR : see 
default address<br>AT+VERSION : See version<br>AT+UART : See baud rate<br>
AT+ROLE: See role of bt module(1=master/0=slave)<br>AT+RESET : Reset and exit AT 
mode<br>AT+ORGL : Restore factory settings<br>AT+PSWD: see default password</span>&nbsp;</p>

<p>
<img
border=0 src="Bouwpakket_files/image048.jpg" class="auto-style1"><img border=0
src="Bouwpakket_files/image049.jpg" class="auto-style1"></p>

</div>

<p><strong>
<br class="auto-style1"><span class="auto-style1">DCF77 ontvangst met DCF-2 
module</span></strong><span class="auto-style1">&nbsp;</span></p>

<p>
<img
border=0 width=450 height=322 src="Bouwpakket_files/DCF-2.jpg"
alt="DCF-2 module" class="auto-style1"></p>

<p class=auto-style1>NB Om het DCF-signaal te kunnen ontvangen is V090 of hoger 
van de woordklok-software nodig.</p>

<p><span class="auto-style1">Deze DCF77-module heeft drie aansluitingen; +, - en 
signal.</span><br class="auto-style1">
<span class="auto-style1">Sluit de + aan op 5V en de - op GND.</span><br class="auto-style1">
<span class="auto-style1">Signal gaat naar pin 2.</span><br class="auto-style1">
<span class="auto-style1">NB Pin 2 werd gebruikt voor de rotary encoderPinB left 
(labeled CLK on decoder). Deze wordt nu aangesloten op P8.</span><br class="auto-style1">
<span class="auto-style1">(Pin 2 is een interrupt pin. Voor een optimale DCF-ontvangst 
is het reageren op een interrupt noodzakelijk voor de rotary encoder niet.</span></p>

<p><span class="auto-style1">Kijk in de source van de versie van de software 
onder "PIN assigments" voor de juiste aansluiting.</span><br class="auto-style1">
<span class="auto-style1">Een<font size="2">, waarschijnlijk goedkope, 12V 220V 
Voeding in de klok stoort de DCF-ontvangst. Gebruik een externe adapter van 'goede' 
kwaliteit.</font></span></p>
	<p class=auto-style1><a href="../DCF77/DCF77_Arduino.html">Hier wat 
	achtergrondinformatie</a> 
	over DCF.<strong><br>&nbsp;</strong></p>

<p class=auto-style2><strong>LED-strips</strong></p>

<p>
<img
border=0 width=650 height=86 id="Picture 55" src="Bouwpakket_files/image004.jpg" class="auto-style1"><br class="auto-style1">
<span class="auto-style1">Onderstaande LEDs worden in de klok voor de 
verlichting van de letters gebruikt.</span></p>

<p><span lang=EN-GB><span class="auto-style1">5M 2835 Cool/Warm White SMD LED 
Non-waterproof 600 led Strip Light</span><br class="auto-style1">
<span class="auto-style1">5M 3528 Cool/Warm White SMD LED Non-waterproof 600 led 
Strip Light</span></span></p>

<p class=auto-style1>De 2835 LED is zuiniger en geeft meer licht. Voor de klok 
maakt het niet uit welke strip genomen wordt. Let er op dat er 120 LEDs per 
meter (600 per 5 meter) zijn en de voedingsspanning 12V is.</p>

<p>E<span class="auto-style1"><strong>nergieverbruik klok</strong></span></p>
<p class=auto-style1>De 30x30 cm klok verbruikt bij 12V met de 3528 LEDs 
minimaal 50 mA als het donker is en de LEDs bijna volledig gedimd zijn . Bij 
volle sterkte loopt het verbuik naar 120mA op.</p>
<p class=auto-style1>Bij het starten, als alle LEDs branden, is het verbruik 
tussen de 200 en 250mA. </p>

