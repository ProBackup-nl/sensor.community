---
title: Saml
---

> ⚠️ **VIGTIG NOTE**
Installer firmwaren, før du samler den!
Se afsnittet __firmware flasher__.

### NodeMCU v3
Bemærk: Vores instruktioner henviser til version 3 af NodeMCU'en. Dette kan genkendes ved forbindelserne VU og G (se tegning).

<img src="../docs/airrohr/airrohr-wiring-sds011-bme280.jpg" style="width:40%; margin-top: 3em" loading="lazy"/>
<small>Copyright: roman-minyaylov, MIT-licens</small>


<img src="../docs/airrohr/nodemcu-v3-bme280.jpeg" style="margin-top: 1em" loading="lazy"/>

#### Når du er færdig, skal det se sådan her ud


### Tilslut SDS011
Pins er nummereret fra HØJRE til VENSTRE, sørg for når du tilslutter kablerne sidder på pinsene, da de fleste Dupont kabler også passer ind mellem pinsene.
```bash
SDS011 Pin 1 -> Pin D1 / GPIO5
SDS011 Pin 2 -> Pin D2 / GPIO4
SDS011 Pin 3 -> GND
SDS011 Pin 4 -> ubrugt
SDS011 Pin 5 -> VU (NodeMCU v3) / VIN (NodeMCU v1,v2)
SDS011 Pin 6 -> ubrugt
SDS011 Pin 7 -> ubrugt
```

<br>

💡 Du kan finde en liste over [sensorer, der understøttes af vores firmware](https://github.com/opendata-stuttgart/sensors-software/blob/master/airrohr-firmware/Readme.md)


### Lodder sammen BME280

<img src="../docs/airrohr/solder-a-bme-280.jpeg" style="width:49%; padding-right: 0.5em" class="items-center" loading="lazy"/>
<img src="../docs/airrohr/solder-bme-280.jpeg" style="width:49%;" loading="lazy"/>

Forbind pin header med BME280-kortet. Lod den fra bagsiden. Hullerne mellem stifterne er meget små, så vær tålmodig og forsigtig.  

Tricket er at sætte loddekolbens spids mod stiften, varme den lidt op og derefter påføre loddet let.  


### Ledninger til BME280
Pins er nummereret fra VENSTRE til HØJRE.
```bash
VIN -> Pin 3V3 (3,3V)
GND-> GND/G
SDA -> PIN D3
SCL -> Pin D4
```

### Bind alt sammen

#### Bind NodeMCU og SDS011 sammen
<img src="../docs/airrohr/tie-air-quality-sensor-together.jpeg" loading="lazy"/>
Brug et kabelbånd til at forbinde NodeMCU'en (ESP8266) og SDS011-sensoren, så Wifi-antennen peger væk fra sensoren

#### Forbind fleksibelt rør
<img src="../docs/airrohr/sds011-with-tube.jpeg" style="width:49%; padding-right: 0.5em" loading="lazy"/>
<img src="../docs/airrohr/bme280-tied-to-tube.jpeg" style="width:49%;" loading="lazy"/>

* Tilslut den fleksible slange til SDS011-sensoren
* Brug et andet kabelbånd til at fastgøre BME280-temperatursensoren til røret
* Før USB-kablet gennem røret. Monter SDS011 med NodeMCU'en vendt mod toppen og blæseren vendt mod bunden
 
#### Skub sensoren ind i røret
* Skub delene ind i røret, så de sidder fast i røret
* USB-kablet, det fleksible rør og BME280 skal kigge ud af rørets ende
* Skub det andet rør på det første.

<img src="../docs/airrohr/sds011-jammed-into-tube.jpeg" loading="lazy"/>

#### Færdiggørelse
* Placér temperaturføleren på det fleksible rør, så den sidder på kanten af røret.
* Skær det fleksible rør af i enden af røret
* Valgfrit: Du kan dække de åbne ender af røret med et fint net. Så kan luften cirkulere, men insekterne bliver udenfor
 
<img src="../docs/airrohr/position-bme280.jpeg" loading="lazy"/>

#### Placering 
Det ideelle sted vil være 1,5 til 3,5 meter over gaden og godt ventileret. Dette kan dog ikke lade sig gøre for alle mennesker, og derfor anmodes der ved registreringen om oplysninger som højde over jorden og placering i forhold til gaden.

