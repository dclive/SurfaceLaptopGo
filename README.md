# SurfaceLaptopGo
Surface Laptop Go bootable EFI
Surface Laptop Go (2020, i5-1035G1) EFI for Hackintosh

All of this is vastly easier if you can work on and create the USB stick on a Macintosh. See my other guide (for example, the Asrock B660M-HDV guide) for full details; this is a high level overview only. The concepts are all exactly the same.

Run GenSMBIOS to find/generate serials (https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/icelake.html#platforminfo), using MacbookAir9,1 as the SMBIOS of choice, as per the Dortania guide.

Put the EFI in place; use OCAT (https://github.com/ic005k/OCAuxiliaryTools) to help with mounting the EFI partition and similar copy operations.

Works: Video, audio, trackpad, touch, wifi, bluetooth.  As of v1.01: sleep/wake work as expected (a little slow, but it works fine), and after first wakeup, brightness works as expected (ie fully bright screen).  

Doesn't work: One should go into System Settings / Trackpad and unselect "Look up and data detectors", as (at least in 12.5.1) leaving this on caused cursor/trackpad irregularities in Finder. 

Made with help from the Dortania Ice Lake laptop guide, https://github.com/olm3ca/Surface-Laptop-Go (for the Ice Lake i5-1035G1 graphics fix .plist), and https://github.com/Xiashangning/BigSurface (for better trackpad, sleep, power - and your USB mapping must be in place for this work well).  Read all three and become familiar with the information in the articles. 

Tested with:  12.5.1.  That's it.  These are early days yet. 

V1.01 Changes: 
1.  Tested very briefly with 12.6.1.  Works great in quick tests. 
2.  USB Mapping put back in place.  Now sleep/wake works and after sleep, brightness is back and looks good!  Big improvement. 
Overall,  a much better experience.  Get v1.01!  Note that in brief testing with 12.6.1, when on battery power, wake doesn't seem to work.  More testing is required.  Please provide any feedback you can. 

For the moment, Ventura (MacOS v13.x) is not recommended, as some issues have been seen with BigSurface.kext in Ventura.  Please hold off updating until the issues are resolved.  For more details on the issue, read https://github.com/Xiashangning/BigSurface/issues/48

Find the EFI folder in the RELEASES.  It's a zipfile.  It needs to go onto the EFI partition, in an EFI folder, with OC and BOOT as the two folders under that EFI folder. 
