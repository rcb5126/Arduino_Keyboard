# Arduino_Keyboard
arduino code for mechanical keyboard made easy

The keyboard I made is a handwired 89 key and is based off of the teensy 2.0++

The code is pretty straightforward. 
Just change your pin declarations, the number of columns and rows, and the FUNCTION_ROW/FUNCTION_COL, and then fill in the corresponding Matrixes with the keycodes.
The Key codes for the teensy I used are here :
https://www.pjrc.com/teensy/usb_keyboard.html

Function key code isn't on the usb_keyboard.html page so I wrote my own support for it. 
I used KC_FN to demark it.

Since the teensy has an led wired to pin_d6 I used that as my CAPSLOCK indicator. 
if you don't want to support an led for CAPSLOCK comment out line 12 of the sketch

#define CAPSLOCK 6 // pin_d6


Also to support function lock: just uncomment line 37 of the sketch
//#define FUNCTION_LOCK
