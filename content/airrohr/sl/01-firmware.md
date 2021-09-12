---
title: Gonilnik in vdelana programska oprema
---

Vdelano programsko opremo smo že pripravili. Namestiti morate le gonilnike in flashniti svoj NodeMCU (ESP8266).

Za komunikacijo s svojo enoto NodeMCU (ESP8266) potrebujete gonilnike usb2serial za svoj operacijski sistem.

Čipni nabor za enote NodeMCU v3 je običajno CH341, za nekaj tehničnih informacij preverite zadnjo stran enote NodeMCU (ESP8266).

Izberite povezavo, ki ustreza operacijskemu sistemu vašega računalnika.

### Windows

#### Gonilniki za NodeMCU (ESP8266) V2 (CP2102) za Windows
* [Windows 10](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip) - sistem Windows 10 bi moral biti sposoben samodejno prenesti te
* [Windows 7/8/8.1](https://www.silabs.com/documents/public/software/CP210x_Windows_Drivers.zip) - 32-bitna različica - **ne podpirajo** 64-bitne različice OS

#### Gonilnik za NodeMCU (ESP8266) V3 (CH340/CH341) za Windows
* [Windows](http://www.wch.cn/downloads/file/5.html) - operacijski sistem Windows 10 bi moral biti sposoben samodejno prenesti te

#### Izvleček prenesene datoteke za Windows
* za NodeMCU (ESP8266) V2: Odprite mapo CP210x in dvakrat kliknite na aplikacijo CP210xVCPInstaller_x64 (ali x86)
* za NodeMCU (ESP8266) V3: odprite mapo CH341SER in dvakrat kliknite na aplikacijo SETUP.

---

### MacOS

#### Gonilniki za MacOS
* [NodeMCU V2](https://www.silabs.com/documents/public/software/Mac_OSX_VCP_Driver.zip)
* [NodeMCU V3](http://www.wch.cn/downloads/file/178.html)

#### Izvleček prenesene datoteke za MacOS
* za V2: Razpakirajte mapo CP210x in dvakrat kliknite na aplikacijo CP210xVCPInstaller_x64 (ali x86)
* za V3: Razpakirajte mapo CH341SER in dvakrat kliknite na aplikacijo SETUP.
* Ponovno zaženite računalnik Mac

---

### Linux
Gonilnikov ni treba namestiti. Čip mora biti podprt neposredno (preverite z dmesg)

---
### Flasher strojne programske opreme
Podpora za več operacijskih sistemov: Windows, MacOS in Linux.

* [airRohr Flashing Tool](http://firmware.sensor.community/airrohr/flashing-tool/)
* [Izvorna koda](https://github.com/opendata-stuttgart/airrohr-firmware-flasher/)

Povežite NodeMCU z računalnikom s kratkim kablom micro-USB (izberite kabel, krajši od 1 metra, sicer namestitev morda ne bo uspešna). Izberite `latest_en.bin` (ali drugo jezikovno različico) in kliknite "Upload".
Počakajte, da se postopek zaključi. Zdaj lahko sestavimo senzor.

#### Linux: Linux: Nastavite dovoljenja kot izvedljivo
Po prenosu boste morda morali nastaviti dovoljenja kot izvršljiva. To lahko storite z ukazom: `chmod o+x <naslov datoteke za prenos>`
<br>
Velika zahvala gre [Piotru, iz Poljske](https://dropbox.inf.re/), za njegovo pomoč! 🙋♂️

#### MacOS: kako zagnati nepreverjeno aplikacijo
Večkrat kliknite z desno tipko miške in odprite aplikacijo ter jo vedno potrdite z "Odpri".

Tukaj je kratek videoposnetek na YouTubu 👉 https://youtu.be/1KZiP94TYjw






