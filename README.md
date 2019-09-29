# moisture_sensor_firmware
This repo is only intended to conveniently create firmware.hex for chirp! and i2c-moisture-sensor.  
Tested with Arduino-1.9.0-beta on MacOS Catalina beta.  

1. Install the Arduino-IDE

2. Add the path:  
Example on the Mac: export PATH=/Applications/Arduino.app/Contents/Java/hardware/tools/avr/bin/:$PATH  

3. Go to the firmware folder an do:  
make hex  

4. Prepare your programmer, which could be an Arduino-ISP  

5. Launch avrdude:  
Example on the Mac: avrdude -C /Applications/Arduino.app/Contents/Java/hardware/tools/avr/etc/avrdude.conf -c avrisp -p t44 -P /dev/cu.wchusbserial1420  -b 19200 -U flash:w:main.hex:i

