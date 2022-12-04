# SurfaceLaptopGo
Early Days - Surface Laptop Go bootable EFI
First attempt: Surface Laptop Go (2020, i5-1035G1) EFI for Hackintosh

All of this is vastly easier if you can work on and create the USB stick on a Macintosh. See my other guide (for example, the Asrock B660M-HDV guide) for full details; this is a high level overview only. The concepts are all exactly the same.

Run GenSMBIOS to find/generate serials (https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/icelake.html#platforminfo), using MacbookAir9,1 as the SMBIOS of choice, as per the Dortania guide.

Put the EFI in place; use OCAT (https://github.com/ic005k/OCAuxiliaryTools) to help with mounting the EFI partition and similar copy operations.

Works: Video, audio, trackpad, touch, wifi, bluetooth.

Doesn't work: Sleep (rather, wakeup) doesn't work. Typical screen rightness is only about 70% of normal.  Brightness controls work, but if set too low, cannot be then increased (requiring a power off/power on). Also, one should go into Trackpad and unselect "Look up and data detectors", as (at least in 12.5.1) leaving this on caused cursor/trackpad irregularities in Finder. 

Made with help from the Dortania Ice Lake laptop guide, https://github.com/olm3ca/Surface-Laptop-Go (for the Ice Lake i5-1035G1 graphics fix .plist), and https://github.com/Xiashangning/BigSurface (for better trackpad, sleep, power - although it seems not to work well at the moment).  Read all three and become familiar with the information in the articles. 

Next steps:  Fix sleep/wake issues, fix brightness issues.  Other than that, it's not a bad laptop. 

Tested with:  12.5.1.  That's it.  These are early days yet. 
