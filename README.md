# DroidScriptBusPirate
DroidScript for easier use of the BusPirate on your Android device.

DroidScript is a free app for Android that lets you write apps in JavaScript / HTML5 /on your phone or tablet/. Let me make that clear... you can /write/ the app on your phone! If you plug in a keyboard, it's even pretty reasonable... but it also allows you to connect your workstation via browser and has a pretty nice IDE. You can always run or share your apps inside DroidScript or for $10, you can turn your DroidScripts into stand-alone real apps. 
http://droidscript.org/
https://play.google.com/store/apps/details?id=com.smartphoneremote.androidscriptfree

BusPirate is a little open source device that connects a USB host device (PC, MAC, or cellphone / tablet via USB OTG) to electronic stuff. It can speak with several different busses (I2C, SPI, UART, etc...) and devices (LCDs, servos, AVRs, FPGAs, CPLDs, etc...) and can inject signals, or measure voltages. It's a little test bench in your pocket for less than $30. 
http://dangerousprototypes.com/docs/Bus_Pirate

The biggest problem with the BusPirate is that on the human side it speaks in very terse, hard to remember, codes. Turning the power on to the circuit under test requires you to enter "W". Setting up to talk to I2C is "m1". You get the idea. 

The point of this script is to make that easy by providing a list of commands, with clear, English, descriptions, which then enter the code for you. You can edit it, then send that code to the device and see the response. If you setup a complex code that you will use often, you can save that code into the list with your own description. 

TODO: 
- Ask for values to enter after the code is selected for those that have parameters. E.g. to generate a pulse train you send "g", but then it wants KHz, and duty cycle. It would be nice to ask for those via a dialog box. 
- Add a 'voltmeter' mode where the ADC reading is repeatedly displayed in large letters, center screen.
- Add scaling to the voltmeter where a potentiometer can be used as a voltage divider to allow voltages higher than +5 to be read. Start by calebrating the scaling by connecting the input to one of the voltage supplies, and turning the potentiometer until the desired voltage is read. E.g. if you want a 1:10 scale, and you connect to the +5 supply, you should read 0.5 volts. Once the unit is calibrated, and the input connected to the device under test, scale the reading to the actual voltage. E.g. if scaled to 1:10, and 1 volt is read on the ADC, display 10 volts. 
- Add a low frequency 'oscilloscope' mode using the binary ADC polling function. There are python scripts for this which can probably be translated.
- Provide some way to share custom codes with other users. 
