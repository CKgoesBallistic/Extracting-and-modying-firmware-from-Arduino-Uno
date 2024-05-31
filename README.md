# Extracting and modying firmware from Arduino-Uno
## Description
- Uses a second arduino uno board as an ISP programmer the extraction and modyification of firmware
- Uses AVRDUDE software and it can be downloaded here : https://github.com/avrdudes/avrdude
- Program the first arduino with any firmare of your choice (Target). Here I have put in the example blink code which blinks the onboard LED every 1000ms.
- Program the second arduino with the ArduinoISP example code (Master)

## Connections to make
| Master Pins | Target Pins|
|-----|------|
|D10| RESET|
|D11|D11|
|D12|D12|
|D13|D13|
|5V|5V|
|GND|GND|

## Extracting the firmware
- After making making the above connections, we can start the extraction process using AVRDUDE software.
```
~$ avrdude -p atmega328p -P /dev/ttyACM0 -c arduino -b 115200 -U flash:r:firmware_backup.hex:i
```
- This would extract the firmware onto an hex file named "firmware_backup"
  
## Modifying the firmware
