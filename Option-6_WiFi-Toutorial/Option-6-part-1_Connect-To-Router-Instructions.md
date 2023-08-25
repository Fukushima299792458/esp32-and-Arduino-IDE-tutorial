# How to connect an esp32 to a WiFi router or a WiFi network.

1. Install the appropriate Arduino IDE version for your device at https://www.arduino.cc/en/software.

2. Copy the code from [HERE](https://github.com/Fukushima299792458/Things-and-stuff/blob/8421117198cfa2a33709255158edd3b28bd47a91/Option-6_WiFi-Toutorial/Option-6-part-1_Connect-To-Router-Demo) into the Arduino IDE. 

3. Then, if you want, read through the comments and extended breakdown [HERE](https://github.com/Fukushima299792458/Things-and-stuff/blob/b7788d807ecc0c25440f35963ac83e259cabdddb/Option-6_WiFi-Toutorial/Option-6-part-1-Code-Breakdown_Connect-To-Router-Demo) for a more in-depth understanding of each of the key WiFi functions.

4. Replace `NetworkName` on line 5 of the code - `const char* ssid = "NetworkName";` - with the name of the network you want to connect to and replace `NetworkPassword` on line 7 of the code - `const char* password = "NetworkPassword";` - with the password of the network you want to connect to.

5. Press `ctrl+shift+B` to open the boards manager, search for "esp32" and install one or both of the options that come up. 

6. Make sure your board is plugged into your computer then make sure it is connected by clicking on the `Tools` dropdown in the top left corner, hover over the `Board: "{may already contain board}"` dropdown, hover over the `esp32` dropdown and select the appropriate board, in this case, the `ESP32 Dev Module`.

7. Connect the port by clicking on `Tools` in the top left again, hover over the `Port: "{may already contain a port}"` and click on the port for your esp32. (If you aren't certain, try removing your esp32 to check which port is the correct port)

9. Press ctrl+U to upload your code to your esp32, wait for it to upload, press `ctrl+shift+M` to open the serial monitor and watch as your esp32 connects to the network. Your esp32 can now connect to WiFi, see part 2 of the tutorial for a modification of this concept.
