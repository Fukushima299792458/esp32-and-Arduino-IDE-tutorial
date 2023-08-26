# WiFi key Functions Breakdown

## SSID
SSID stands for Service Set IDentifier, this is the display name for your WiFi network so `const char* ssid = "NetworkName";` on line 5 should contain your network name (maximum of 63 characters), and `const char* password = "nononono";` on line 7 should contain your network password (minimum of 8 characters or set null to have no password).

## `WiFi.mode()`
`WiFi.mode()` sets the way the esp32 should act with different WiFi functions and changes what functions can be used. There are three possible inputs for this function;

1. `WIFI_STA` sets the esp32 to a WiFi station which means it will be able to connect to a router/AP(Access Point, see second possible mode)/WiFi network. While in station mode, the `WiFi.begin()` and `WiFi.localIP()` functions can be used (see the `WiFi.begin()` and `WiFi.localIP()` sections respectively).

2. `WIFI_AP` makes the esp32 an Access Point, which means it will act as a router/AP(Access Point)/WiFi network/WLAN without internet. As an access point, the `WiFi.softAP()` and `WiFi.sofAPIP()` functiions are available (see the `WiFi.softAP()` and `WiFi.softAPIP()` sections respectively).

# 3. `WIFI_AP_STA` makes the esp32 both an Access Point and a WiFi station, which means it will act as a router/AP(Access Point)/WiFi network/WLAN without internet. As an access point and a WiFi station, the esp can use all of the WiFi functions.

### `WiFi.begin()`
`WiFi.begin()` tells the WiFi station to try to connect to a WiFi network. The `WiFi.begin()` function takes two arguments to set the network name, or as in the example code, `ssid`, and the network password, in the code as password or `WiFi.begin(ssid, password);`. 
  - Can take one argument if the network doesn't have a password as just `WiFi.begin(ssid);`. 
  - Can also take three arguments of `WiFi.begin(ssid, keyIndex, keys);` which uses a key in the keys array based on the keyindex and is used for WPA encrypted networks but is outside the scope of this tutorial.

### `WiFi.localIP()`
`WiFi.localIP()` returns the local IP address of the WiFi station on the WiFi network it is connected to and may be useful for WiFi server applications that are outside the scope of this tutorial. 

### `WiFi.softAP()`
`WiFi.softAP()` tells the esp32 to start broadcasting as a WiFi network or access point. The `WiFi.softAP()` function takes two arguments to set the network name, or as in the example code, `ssid`, and the network password, in the code as password or `WiFi.softAP(ssid, password);`. 
  - Can take one argument if you don't want the network to have a password, as just `WiFi.softAP(ssid);` or it can take a null `""` as a placeholder for the password. 
  - Can also take five arguments of `WiFi.begin(ssid, password, channel, hiddenSSID, maxConnections);` which uses forces the WiFi `channel` or sub bandwidth you want (from 1-13), makes the network a visible network or hidden network (0-1 respectively), and `maxConnections` dictates how many people can join the network at once (1-10 but 1-4 is recommended depending on specific board specifications).

### `WiFi.softAPIP()`
`WiFi.softAPIP()` returns the IP address of the WiFi router to be accessed on its WiFi network and may be useful for WiFi server applications that are outside the scope of this tutorial. 
