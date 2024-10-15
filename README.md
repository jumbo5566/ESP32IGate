# ESP32IGate Simple Project

ESP32IGate is a Internet Gateway(IGate)/Dital Repeater(DiGi)/Tracker/Weather(WX)/Telemetry(TLM) with TNC Built in that is implemented for Espressif ESP32 processor.
 

## Feature

* Inside RF Module: SR110_VHF or SR110_UHF (500mw LOW or 1w HIGH) 
* Support APRS internet gateway (IGATE)
* Support APRS digital repeater (DIGI)
* Support APRS tracker (TRACKER)
* Support GNSS External mod select UART0-2 and TCP Client
* Support TNC External mod select UART0-2 and Yaesu packet
* Support APRS IGATE/DIGI/WX with fix position for move position from GNSS
* Support AFSK 1600/1800Hz 300bps AFSK (For HF radio)
* Support AFSK Bell202 1200bps (For VHF/UHF radio)
* Implementing software modem, decoding and encoding
* Support monitor display information and statistices
* Support Wi-Fi multi station or WiFi Access point
* support Web Service config and control system
* support filter packet rx/tx on igate,digi,display
* support audio filter BPF,HPF
* support VPN wireguard
* support global time zone
* support web service auth login
* display received and transmit packet on the LED and display OLED

## Hardware screen short
![esp32dr_simple](image/ESP32DR_Simple_Test.png) ![esp32dr_sa868](image/ESP32DR_SA868_2.png)
![esp32dr_sa868_pcb](doc/ESP32DR_SA868/ESP32DR_SA868_Block.png)

## Hardware mod
![esp32dr_sql](image/ESP32IGate_SQL.jpg) 

## Web service screen short
![screen_dashboard](image/ESP32IGate_Screen_dashboard.png) ![screen_igate](image/ESP32IGate_Screen_igate.png) \
![screen_radio](image/ESP32IGate_Screen_radio.png) ![screen_mod](image/ESP32IGate_Screen_mod.png)


### Schematic


## ESP32IGate firmware installation (do it first time, next time via the web browser)
- 1.Connect the USB cable to the ESP32 Module.
- 2.Download firmware and open the program ESP32 DOWNLOAD TOOL, set it in the firmware upload program, set the firmware to ESP32IGate_Vxx.bin, location 0x10000 and partitions.bin at 0x8000 and bootloader.bin at 0x1000 and boot.bin at 0xe000, if not loaded, connect GPIO0 cable to GND, press START button finished, press power button or reset (red) again.
- 3.Then go to WiFi AP SSID: ESP32IGate and open a browser to the website. http://192.168.4.1 password: aprsthnetwork Can be fixed Or turn on your Wi-Fi router.
- 4.Push **BOOT** button long >100ms to TX Position and >10Sec to Factory Default

![ESP32Tool](image/ESP32Tool.png)

## ESP32 Flash Download Tools
https://www.espressif.com/en/support/download/other-tools


## PlatformIO Quick Start

1. Install [Visual Studio Code](https://code.visualstudio.com/) and [Python](https://www.python.org/)
2. Search for the `PlatformIO` plugin in the `VisualStudioCode` extension and install it.
3. After the installation is complete, you need to restart `VisualStudioCode`
4. After restarting `VisualStudioCode`, select `File` in the upper left corner of `VisualStudioCode` -> `Open Folder` -> select the `ESP32APRS_T-TWR` directory
5. Click on the `platformio.ini` file, and in the `platformio` column, cancel the sample line that needs to be used, please make sure that only one line is valid
6. Click the (✔) symbol in the lower left corner to compile
7. Connect the board to the computer USB
8. Click (→) to upload firmware and reboot again
9. After reboot display monitor and reconfig

## APRS Server service

- APRS SERVER of T2THAI at [aprs.dprns.com:14580](http://aprs.dprns.com:14501)
- APRS SERVER of T2THAI ampr host at [aprs.hs5tqa.ampr.org:14580](http://aprs.hs5tqa.ampr.org:14501)
- APRS MAP SERVICE [http://aprs.nakhonthai.net](http://aprs.nakhonthai.net)

## ESP32 Flash Download Tools
https://www.espressif.com/en/support/download/other-tools

## Credits & Reference

- ESP32TNC project by amedes [ESP32TNC](https://github.com/amedes/ESP32TNC)
- APRS Library by markqvist [LibAPRS](https://github.com/markqvist/LibAPRS)

## HITH
This project implement by APRS text (TNC2 Raw) only,It not support null string(0x00) in the package.
