# Micropython code
First program the micropython firmware on your ESP8266 board so that python code can be executed. Docs are available on the microphython web site.

https://docs.micropython.org/en/latest/esp8266/tutorial/intro.html

Uploading the files to the ESP8266 device. Check which device your ESP8266 gets in your OS (different under linux / OS-X).

# gpio-wget example
This example is using a GPIO state change to trigger a wget. Useful when you have a GP-out in any system that you want to turn into a http request for controlling anything (enabling somethinng when turning on the burglar alarm or similar).

Example of a config.json
'''
{
    "SSID": "your-wifi-ssid",
    "password": "your-wifi-password"
}
'''


    >ampy --port /dev/ttyUSB0 --baud 115200 put main.py
    >ampy --port /dev/ttyUSB0 --baud 115200 put config.json

Checking which files are on your ESP8266 can be done via ampy also:

    >ampy --port /dev/tty.SLAB_USBtoUART --baud 115200 ls
    /boot.py
    /config.json
    /main.py


Ampy is available as arduino-ampy, see this for install instructions:

https://learn.adafruit.com/micropython-basics-load-files-and-run-code/install-ampy

>ampy --port /dev/ttyUSB0 --baud 115200 put main.py


Then just reboot the device an
