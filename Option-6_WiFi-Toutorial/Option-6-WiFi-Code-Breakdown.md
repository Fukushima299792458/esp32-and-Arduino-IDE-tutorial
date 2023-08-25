# WiFi key Functions Breakdown

## SSID
SSID stands for Service Set IDentifier, this is the display name for your WiFi network so `const char* ssid = "NetworkName";` on line 5 should contain your network name.

## `WiFi.mode()`
`WiFi.mode()` sets the way the esp32 should act with different WiFi functions and changes what functions can be used. There are three possible inputs for this function;

1. `WIFI_STA` sets the esp32 to a WiFi station which means it will be able to connect to a router/AP(Access Point, see second possible mode)/WiFi network. While in station mode, the `WiFi.begin()` and `WiFi.localIP()` functions can be used (see the `WiFi.begin()` and `WiFi.localIP()` sections respectively).

2. `WIFI_AP` makes the esp32 an Access Point, which means it will act as a router/AP(Access Point)/WiFi network/WLAN without internet. As an access point, the `WiFi.softAP()` and `WiFi.sofAPIP()` (see the `WiFi.in()` and `WiFi.softAPIP()` sections respectively).

