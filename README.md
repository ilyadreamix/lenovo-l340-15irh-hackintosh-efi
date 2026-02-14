

### What works
|Type|Name|Note
|---|---|---|
|CPU|Intel Core i7-9750|Native. No problems at all|
|iGPU|Intel UHD 630|Works perfect. No problems at all|
|Wi-Fi|TP-Link Archer T2U Nano|USB Wi-Fi adapter, had to use [Wireless USB OC Big Sur Adapter](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter)|
|SSD|Union Memory RPFTJ256PDD2MWX|Works fine|
|Audio|Realtek ALC257|Works fine|

### What does NOT work
|Type|Name|Note
|---|---|---|
|dGPU|Nvidia GTX 1650|Had to disable with custom SSDT-dGPU-Off.aml (also with -wegnoegpu boot flag)|
|Trackpad|ELAN 0627|Pure devil's shit. See comments below|
|Wake|❌|See comments below|

### Additional notes

#### Trackpad
Spent 2 days trying to figure out how to get it work (patched ELAN0626 via GPIO 0x4B, tried -vi2c-force-polling boot argument and VoodooI2CELAN.kext).
It wasn't worth the hassle. The best behavior I've got was unusable drunk-drifting cursor

#### Wake
I've successfully mapped all USB ports, so my laptop could enter sleep mode, but it wasn't able to wake back.
I decided to let it go
