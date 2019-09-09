Compilation instructions

1.  Install Arduino IDE
    You get the latest Arduino IDE here:
    http://arduino.cc/en/Main/Software

    You need at least 1.0 for the Atmel AVR based boards and 1.5 for the ARM based boards like the due.

2.  Make sure the serial driver for your printer board is installed. The Arduino IDE contains signed drivers
    for the Arduino boards. Depending on your board you might need different drivers then these. For Linux and Mac
    you often do not need any additional drivers. Ask your printer/board vendor which driver you need,
    if that is not clear to you.

3.  Some boards that are not original arduino boards and not 100% compatible to them, need separate extensions
    to the Arduino IDE. Install them.

4.  Start Arduino IDE and open the file "Repetier.ino"

5.  Select the board and port for upload in the arduino ide.

6.  Check Configuration.h for hints, if something needs to be checked or modified.

7.  Upload the firmware with the upload button (right arrow in toolbar).

If you have a normal mega 2560 compatible board, you can use codeblocks for arduino instead of the arduino ide:
http://arduinodev.com/codeblocks/
Open the Repetier.cbp file instead of the ino file and start with 6.

HINT: It you have enabled eeprom support, the first upload will copy the configurations into the eeprom. Later
uploads will NOT overwrite these settings! Connect with Repetier-Host to your printer and open the eeprom editor
to change these values. Alternatively, send the commands
 M502
 M500
to copy the new values in Configuration.h to eeprom.


IMPORTANT FOR DUE USERS

There is an additional folder AdditionalArduinoFiles with separate readme that describes how to get
watchdog working. It is a very good idea to compile with working watchdog!!!

===
Tips:
1. The board for the 3D printer is the RAMBo v1.4 See specs here:
   https://reprap.org/wiki/Rambo_v1.4
   
2. Use Repetier-Firmware Configuration Tool to change the repetier firmware
   https://www.repetier.com/firmware/v092/
   
3. Pronterface.exe is a frontend software used for testing the printer:
   https://www.pronterface.com/

4. Repetier-Host is the preferred frontend software:
   https://www.repetier.com/download-now/

