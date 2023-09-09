# ESP32-Prop-Controller

This code is for a multi-prop controller on an ESP32 using Arduino IDE. 
Watch the How-To Video at Casual Haunter on youtube. 

Install Arduino IDE

// This will add the ESP32 capability to Arduino IDE
In Adruino IDE go to File > Preferences: Go to Addition Boards Manager URL and paste https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
Click OK

// This will add the ESP32 DEVKIT V1 to your Arduino IDE options
Go to Tools > Board > Board Manager
Search ESP32
Install esp32 by Espressif Systems

// This will install the USB driver to connect the esp32 to windows
Go to https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads
Download CP210x Universal Windows Driver
Unzip it and open up the folder
Right click on silabser.inf and click install

// This will tell Arduino what board and how to connect it
Go to Tools > Board and select DOIT ESP32 DEVKIT V1
Go to Tools and choose Com3 (or 4 or whatever works here)
Connect your ESP32 DEVKIT V1 with a USB micro cable to your computer

// Add the library for the web server, ESPAsyncWebServer
Go to this link and download this zip https://github.com/me-no-dev/ESPAsyncWebServer/archive/master.zip
In Arduino IDE go to Sketch > Include Library > Add .zip Library
Choose the .zip file you just downloaded. There is no need for an unzipping program

Copy and paste the code from MultiPropControllerv1.txt into Arduino IDE 
Change your WIFI name and password
Set the static IP of your choice and add the gateway IP with correct subnet mask
Set your router to have a range of statics available
Upload the code to the ESP32

In any browser, type in the IP address you put into the program 
Follow the video on how to set up and use the board

Available pins for triggering animatronics 
D4, D13, D14 D18, D21, D22, D23, D25, D26, D27, D32, D33

Availabe pins for triggering a relay
RX2, TX2

Availabe pin as a pass through to connect a step pad
D19
D19 will trigger D21 ONLY as well as allowing D21 to accept GET URL triggeres

