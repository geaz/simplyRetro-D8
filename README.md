[![3D2P](https://img.shields.io/badge/3D2P-simplyRetro%20D8-orange.svg)](https://3d2p.net/Project/LY2PZWIBBV0WRMZCS59JRB)
[![Thingiverse](https://img.shields.io/badge/Thingiverse-simplyRetro%20D8-blue.svg)](https://www.thingiverse.com/thing:4295854)
[![Github](https://img.shields.io/badge/Github-simplyRetro%20D8-brightgreen.svg)](https://github.com/geaz/simplyRetro-D8)

This repository contains everything to rebuild the *simplyRetro D8*.
The *D8* is my first attempt to build a small custom bartop from scratch.
It runs a custom linux image for emulation to accomplish a fast boot time (10 seconds).
But you are also able to use Retropie or Lakka for example.

![simplyRetro D8](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/cover.jpg)

You can find a small video of it in action on [Youtube]().

## Warning
This is a quite an easy build which is not using many screws and minimal soldering, but some of the screws are very hard to reach.
**I don't think you are able to pull of this build without the usage of a ratchet!**
I wanted a build without any visible screws and minimal amount of parts which are able to break. There is surely a way to accomplish these tasks with better screw holes. If you know one, you are free to edit the model (Fusion 360 Archive File in the CAD folder).

## Features
- Custom 3D printed shell
- Custom linux distribution for fast boot
- Stereo Speakers and Volume Control
- 12 Buttons
- 8 inch display
- Raspberry Pi 2 or 3 powered

## 3D Model
The model was designed in Fusion360. The STLs are in the Thingiverse downloads and the Github repository. Furthermore there is an exported Fusion 360 Archive File ready to download.

## BOM

- 3D Printed Shell (STL folder for models)
- [8 inch HDMI IPS Display](https://de.aliexpress.com/item/32325920866.html) (If you want to use another display, make sure to adapt the shell) 
- [1x PAM8403](https://de.aliexpress.com/item/32452488898.html?spm=a2g0s.9042311.0.0.1df04c4dcQesbB)
- [1x Arcade Controller Set](https://www.amazon.de/gp/product/B01N78D6HB) (If you want to use the custom arcade button housing I used, this set is fine. If you want to use original arcade buttons, get buttons with a 24mm mounting diameter! Otherwise they won't fit into the holes!)
- 1x Raspberry Pi 2 or 3
- 1x Power Adapter
- [2x Speaker](https://www.reichelt.de/kleinlautsprecher-k-34-wp-1w-8ohm-vis-2981-p204642.html?&trstct=pos_0) (or similar, just make sure they have a diameter of 3.4 cm or adapt the shell)
- 1x Audio Jack (male)
- 1x HDMI Cable (get a short one - the shell will already be quite crowded)
- 1x USB Type A to USB Type B (for arcade controller connection - see HDMI Cable note above) 
- Wire
- 12x M3x8mm screws
- Zip Ties
- Velcro or double-faced adhesive tape to attach the PAM, Arcade Controller Board and Display Board
- Wire :)

## Build

**For the first part you have to use a ratchet. I don't think that all screws are accessible without one!** 

### Shell

To make your life a bit easier, preinsert eight screws into the holes of the *Back Panel* and *Front Panel*. Furthermore I recommend to widen the first millimeter of the holes on the side panels a bit. 

![Screw in Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/1.jpg)

Screw the *Front Panel* and *Back Panel* to one of the side panels. Then insert the display into the slot and screw the remaining side panel. **The last top screw of the *Back Panel* will be painful! Use your ratchet!**

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/2.jpg)

### Arcade Stick

To fit the arcade stick into the shell you have to remove the mounting plate and do something about the two holes (see picture - I added a red circle on one of them). You have two options here:

1. Use the controller in the direction it was intended, but you will have to remove the two little holes. Otherwise it won't fit into the shell.
2. Remove the transparent part at the bottom, remove the circuit with the switches and rotate it by 90°. This way it will fit, but you have to rebind the arcade stick controls in your OS later.

I went for option two. My controller board had a defect and I was not able to use the *select* button plug. Thats why I had to remap the arcade controls either way.

![Arcade Stick](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/3.jpg)

You should be able to use the screws of the mounting plate to mount the stick to the shell.

![Arcade Stick](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/4.jpg)

Add the *Duster* and screw the *Joystick Ball* to the top of the stick.

![Joystick Ball](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/5.jpg)

### Buttons

**If you want to use original 24mm arcade buttons, you are free to skip this section.**

You have to disassemble the arcade buttons to use the custom housing. Remove the top of the buttons and use a caliper to press the led circuit out of the housing. Removing the switch should be straight forward (a flat screwdriver helps).

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/6.jpg)

First insert the switch to the custom housing (take note of the orientation in the following pictures). If you want/need it, use a bit of glue to mount the switches. Then insert the led circuit. This will be a tight fit. Use a bit force if necessary (or *The Force*
, if it helps).

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/8.jpg)

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/7.jpg)

Insert the *Button Top*s into the *Front Panel* and mount the *Button Housing*s. Same goes for the *Side Button Top*s.

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/9.jpg)

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/10.jpg)

After wiring the buttons bend the pins a bit. Otherwise you won't be able to close the shell in the last step.

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/13.jpg)

### Audio

Take the pictures as a reference for the audio *circuit*. This should be straightforward. The top part of the audio jack is the *Left* channel, the middle part the *Right* channel and the bottom part is *Ground*. Insert the speakers into the *mounting circles* of the *Back Panel*. Just use a drop of hot glue, if it is not a press fit in your case. Mount the PAM to the *Back Panel*.

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/11.jpg)
![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/12.jpg)

### Raspberry Pi and closing the shell

Mount the Raspberry Pi to the *Bottom Panel* and insert the power adapter, HDMI and USB plugs into it (Arcade Controller and Display). Don't forget to zip tie the power adapter cable to secure it (see picture). 

![Shell](https://raw.githubusercontent.com/geaz/simplyRetro-D8/master/images/Internals.jpg)

Now configure your retro system as you want and close the shell. You are done!

## Custom Distribution
The custom distribution can be downloaded [here](https://github.com/geaz/simplyRetro-D8/releases).  
It is based on [BuildRoot](https://buildroot.org/) and just contains the packages needed to play on the *D8*. 

**Please be aware, that the distribution was build for the D8! It was not tested as a standalone distribution.**

The *D8* uses Retroarch for all emulations. The following systems are supported at the moment (more can be added):

- Arcade (MAME2013-plus - BIOS needed)
- Gameboy DMG / Color (Gambatte)
- Gameboy Advance (gpsp - BIOS needed)
- NES (quicknes)
- SNES (snes9x2002)
- Meda Drive / Master System / Sega CD (picodrive - BIOS needed for Sega CD)

If you want to use the distribution just use Etcher to copy the img file to a SD Card.
The root password is 'simplyretro'.

### Resize Root
To use the full size of you SD Card you should execute the following two scripts in order:

/root/reformat.sh (will reboot the system after execution)  
/root/resize.sh

### WiFi & Services
You are able to set your WiFi SSID and PSK through the Emulationstation menu. Press 'Start' and go into the 'simplyRetro' menu.
After setting the WiFi, just enable any service you need. **I recommend to disable the services after usage to speed up the boot process.**

### ROMs and BIOS folder
The ROMs and BIOS folder are located at */root/roms* and */root/bios*. You are able to change the splash screen, if you want. It is also located at the */root* folder. Use the FTP service to copy your roms to the *D8*.

### Controls
EmulationStation will ask you to configure your controller on the first start.  
Retro Arch is configured to exit a ROM, if you press *START + B*.  
You are able to open the Retro Arch menu while playing a game, if you press *START + A*.

### Updates
If there will be an update to the distribution, I will try to distribute the updated files together with the image. This way you are able to update just these files via FTP and don't have to flash the whole image again.

## Credits
Thanks to [BuildRoot](https://buildroot.org/) for the creation of this great system which enabled me to create a custom linux distribution.  
Thanks to [RecalBox](https://www.recalbox.com/) for their work on the packages for BuildRoot. I took the RetroArch and LibRetro packages and reworked them a bit to work on my distribution. Also thanks for the code of the on screen keyboard!