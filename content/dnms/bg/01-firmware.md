---
title: Драйвер и фърмуер
---
Вече сме подготвили фърмуера. Трябва само да инсталирате драйвери и да флашнете вашите платки NodeMCU (ESP8266) и Teensy 4.0.

За да комуникирате с вашия ESP8266, се нуждаете от usb2serial драйвери за вашата операционна система.

Чипсетът за NodeMCU v3 обикновено е CH341, просто проверете на гърба на вашия NodeMCU, за да намерите някаква техническа информация. Изберете връзката, която съответства на операционната система на вашия компютър.

### Windows

#### Драйвери за модел V2 (CP2102) за Windows
* [Windows 10](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip) - Windows 10 би трябвало да може да ги изтегли автоматично
* [Windows 7/8/8.1](https://www.silabs.com/documents/public/software/CP210x_Windows_Drivers.zip) - 32-битова версия - **не се поддържа** 64-битова версия на операционната система

#### Драйвер за модел V3 (CH340/CH341) за Windows
* [Windows](http://www.wch.cn/downloads/file/5.html) - Windows 10 би трябвало да може да ги изтегли автоматично

#### Извличане на изтегления файл за Windows
* за V2: Отворете папката CP210x и щракнете два пъти върху приложението CP210xVCPInstaller_x64 (или x86)
* за V3: отворете папката CH341SER и щракнете два пъти върху приложението SETUP.

---

### MacOS

#### MacOS драйвери
* [NodeMCU V2](https://www.silabs.com/documents/public/software/Mac_OSX_VCP_Driver.zip )
* [NodeMCU V3](http://www.wch.cn/downloads/file/178.html)

#### Извличане на изтегления файл за MacOS
* за V2: Разопаковайте папката CP210x и щракнете два пъти върху приложението CP210xVCPInstaller_x64 (или x86)
* за V3: разархивирайте папката CH341SER и щракнете два пъти върху приложението SETUP.
* Рестартирайте вашия Mac

---

### Linux
Не е необходимо да се инсталират драйвери. Чипът трябва да се поддържа директно (проверява се с dmesg)

---
### Флашър за фърмуер NodeMCU
Поддръжка на множество операционни системи: Windows, MacOS и Linux.

* [airRohr Flashing Tool](http://firmware.sensor.community/airrohr/flashing-tool/)
* [Изходен код](https://github.com/opendata-stuttgart/airrohr-firmware-flasher/)

Свържете NodeMCU към компютъра си с къс micro-USB кабел (изберете такъв, който е по-къс от 1 метър, в противен случай инсталацията може да се провали). Изберете `latest_en.bin` (или друга езикова версия) и щракнете върху "Upload" (качване).
Изчакайте, докато процесът приключи. Сега можем да сглобим сензора.
<br>
Голяма благодарност на [Пьотр, от Полша](https://dropbox.inf.re/), за помощта му! 🙋♂️

---
### Флашър за фърмуер Teensy
В Github на [Helmut Bitter](https://github.com/hbitter/DNMS/tree/master/Firmware) можете да намерите два вида фърмуер:
* .ino
* .hex

#### Teensy Loader
Можете да флашнете .hex файла в платките Teensy със самостоятелния софтуер с графичен интерфейс [Teensy Loader](https://www.pjrc.com/teensy/loader.html) за Windows, Mac и Linux.
Съществува и версия за команден ред.

#### Teensyduino
Можете да флашнете .ino файла в платките Teensy с разширението Arduino IDE [Teensyduino](https://www.pjrc.com/teensy/teensyduino.html).
Ако е необходимо, можете да модифицирате фърмуера директно в Arduino IDE.