# What

## WiFi Ship

Arduino (ESP8266) library providing API to WiFi connection.

(2023-12 .. 2024-02, 2024-05)


## Overview

Esplora WiFi API wrapper.

  - [x] Get/set MAC
  - [x] Scan
  - [x] Connect to router
  - [x] Get IP

Do it with style!

I love space games (Elite, KSP), so imagining my WiFi module as _Ship_
(base type is _Craft_).

Ship has _Name_ (SSID) and _Id_ (MAC). It can _Scan_ space for _Stations_
(routers) to _Dock_ (connect) with them.


## Demo output

Real output for my case. Sensitive information from scanner and docker
is manually substituted to `*`.

```
Demo of <me_WifiShip.h>.

Main loop interval (s): 90

----------------------( Core test )------------------------------
We are getting ship's id and name, changing em and getting again:

Id: 3C:71:BF:29:2A:AF
Name: ESP-292AAF

Id: DE:FA:CE:D0:00:00
Name: REBORN
----------------------( Core test done )-------------------------

----------------------( Scanner test )---------------------------
We will scan ether for stations, sort them by signal strength and
display results.

Signal | Protocol |        Id         |           Name
-------+----------+-------------------+---------------------------------
   -30 | WPA2     | 74:DA:**:**:**:** | ************
   -64 | WPA2     | 34:60:**:**:**:** | **********
   -66 | WPA1/2   | D0:B6:**:**:**:** | *****************
   -71 | WPA1/2   | B4:A5:**:**:**:** | ************
   -79 | WPA2     | 52:FF:**:**:**:** |
   -79 | WPA2     | 52:FF:**:**:**:** | *********
   -83 | WPA1/2   | BC:0F:**:**:**:** | ************
   -87 | WPA2     | 50:FF:**:**:**:** | *********
   -89 | WPA1/2   | 60:CE:**:**:**:** | **********
   -92 | WPA2     | 52:FF:**:**:**:** |
------------------------------------------------------------------------
10 stations
----------------------( Scanner test done )----------------------

----------------------( Docker test )------------------------------
Test of docker module.

We are trying to connect to preset station with preset password.
In case of success, we will print ship address and station address.
We will disconnect afterwards.

Station name: **********
Station password: *********
Status: Docked
Ship address: 192.168.0.116
Station address: 192.168.0.1
Status: Undocked
----------------------( Docker test done )-------------------------
```

[Example code](examples/me_WifiShip/me_WifiShip.ino)

Tested on "LOLIN(WeMos) D1 R1" (esp8266:esp8266:d1).


## See also

[My other repositories][repos].

[repos]: https://github.com/martin-eden/contents
