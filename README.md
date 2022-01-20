# LoLCon
A fork of erikmwerner's <a href="https://github.com/erikmwerner/QJoyControl">QJoyControl<a> modified with a specific scheme for playing League of Legends using left joycon and mouse. This allows you to use the joystick to move and control cast directions with the mouse.
  * Analog stick clicks rapidly in a circle around the champion, and clicks on the champion when centered. Naturally, this means you must play with fixed camera on.
  * Abilities can be used through binding joycon buttons. When a button is held or the mouse clicked, the analog stick is ignored, so your ability will cast towards your cursor. 
    * A cool option here is to bind a mouse button to attack only, theoretically allowing for easy kiting.
    * Use capture button to switch between Red and Blue teams, as each team has a different centering on screen.
  * Currently functions only on MacOS. However, the only architechture-specific code is the mouse events.
  
  Planned future features:
  * Less crappy UI menus as I learn QT
  * Allowing for specific buttons to not disable the joystick, letting them be used as toggles and such. 
  * Try using AppleScript instead of CGEvents to click (if it works), allowing for true separation of mouse from stick movement (no more moving the mouse rapidly back and forth)
  * Extend to other OSes, automatic screen resolution handling
  * Add mouse centering settings to the UI to support computers with different resolutions or windowed mode. 
  * Right joycon support for directional ability casts, autos, generally having more buttons
  * Tilt controls? Shake to dance? Rumble?



# QJoyControl <img src="https://github.com/erikmwerner/QJoyControl/blob/master/img/Logo.png" align="left" width="64" height="64" title="">
QJoyControl lets you use Nintendo Switch JoyCons as input devices on your computer. It was originally made to use a JoyCon as a PowerPoint remote, but it accumulated a few extra features along the way. Currently, QJoyControl supports:
* JoyCons and Pro Controller
* Mouse control with analog sticks and gyroscope
* Adjustable mouse sensitivity
* Configurable button-to-key mapping
* Image capture with the IR Camera
* Rumble and player LED commands

It also works pretty well as a PowerPoint remote.

## Setup
1. Pair the JoyCon with your computer and connect to it with bluetooth
   * To pair, press the pairing button on the JoyCon and go to Bluetooth Preferences on your Mac
2. Open QJoyControl and select the JoyCon from the device list
   * If nothing shows up, make sure the JoyCon is paired and connected and click Refresh to check again
3. Click Connect to begin streaming input data

If MacOS does not ask to give QJoyControl permission to control your computer, you may need to go into System Preferences and do it manually before keyboard and mouse inputs will register with MacOS. To do this, go to System Preferences, Security & Privacy > Privacy > Accessibility. From there, click the lock icon in the bottom-left corner, enter you password to unlock, click the plus button, and select QJoyControl to add QJoyControl to the list of approved applications.

## Compatibility
QJoyControl should work on MacOS 10.7 and later, although it has only been tested on MacOS 10.13 and 10.14. QJoyControl was written with Qt and [hidapi](https://github.com/signal11/hidapi) for cross-platform support. It should eventually work on MacOS, Windows, and Linux, but at the moment only MacOS support is implemented.

## Thanks
* All of the HID communication came from the hard work at [JoyCon Reverse Engineering](https://github.com/dekuNukem/Nintendo_Switch_Reverse_Engineering)
* The IR camera features came from the excellent [Joy-Con Toolkit](https://github.com/CTCaer/jc_toolkit)

## Disclaimer
This project is not endorsed by, affiliated with, maintained, authorized, or sponsored by Nintendo. All product and company names are the registered trademarks of their original owners. The use of any trade name or trademark is for identification and reference purposes only and does not imply any association with the trademark holder of their product brand.

