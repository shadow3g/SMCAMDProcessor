SMCAMDProcessor
========

AMD Processor power management and system monitoring plugin for [VirtualSMC](https://github.com/acidanthera/VirtualSMC).


Please note that this release is at very initial stage of development, make sure you have a proper backup of your EFI folder and never run on any system that matters. 


### Now with AMD Power Tool
<img src="imgs/all.png" width="80%">

## Installation

1. Download kext and application from [Release](https://github.com/trulyspinach/SMCAMDProcessor/releases) page
2. Add SMCAMDProcessor.kext to kext folder of your bootloader.
3. Edit your bootloader's config file to make sure the kext is enabled.
4. Done!

## Features
* Passive CPU power management. 
* Supports for reading of temperature, energy and clock data on AMD 17h Processors.
* Manual switching of processor speed with AMD Power Tool.

## Passive Power Management
This options serves as a temporary solution to CPU power management due to no active solution are currently available. Comparing to a true active power managment implementation, this option works in a passive way which results in less sensitivity, accuracy and a slow down in performance.

I have been exploring possibilities for implementing a real active power management solution for AMD 17h platform. From what it looks like currently it is definitly possible. I will keep updating here with my latest progress.

<img src="imgs/ani.gif" width="100%">


## Editing PState

Since the release 0.3.1, you can now edit your CPU PState using AMD Power Tool.
<img src="imgs/pe.png" width="60%">

To access PState editor:
1. Open AMD Power Tool
2. Go to 'Speed' tab
3. Click 'Advanced Options'

#### Safety Notes
* Incorrect PState setting can potentially cause permanent damage to your computer hardware.
* For safety concern, this function was limited to root user only. You can either launch AMD Power Gadget with root user or use `-amdpnopchk` to disable this check.



## Tested Processors
* Ryzen 9 3900X
* Ryzen 7 3700X
* Ryzen 7 2700X
* Ryzen 5 3600
* Threadripper 2990WX

<img src="imgs/iStats.png" width="40%">

## What's Coming?

* PState Editing, a direct editing of PState definition may open up possibilities for overclocking in macOS.
* Active Power Management.


## Contribution
#### If you want to support this project, please:

* Give it a star! 😄
* Feel free to open up an issue if it works for you and not listed on supported processors.
* or if something breaks, please also open an issue.

* If you like to help with some coding, feel free to submit any pull request or just DM me on Discord.

## Credits
* [necross2](https://github.com/necross2) for adding support to temperature sensor offset.
* [Shaneee](https://github.com/Shaneee) for the beautiful icon.

## Notes
* I am still fairly new to macOS kernel development, this software project was initally a hobby project to get some reading on my newly built AMD hackintosh computer.

* With that being said, please bear with some of the spaghetti and not-idiomatic codes. Any criticism is much welcomed :)
