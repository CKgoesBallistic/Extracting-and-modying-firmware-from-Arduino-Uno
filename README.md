# Extracting and modying firmware from Arduino-Uno
## Description
- Uses a second arduino uno board as an ISP programmer the extraction and modyification of firmware
- Uses AVRDUDE software and it can be downloaded here : https://github.com/avrdudes/avrdude
- Program the first arduino with any firmare of your choice (Target)
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

