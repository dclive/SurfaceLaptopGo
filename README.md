# SurfaceLaptopGo
Surface Laptop Go bootable EFI
Surface Laptop Go (2020, i5-1035G1) EFI for Hackintosh
V1.10 EFI for Ventura (the issue: check airportitwlm if you use another MacOS version; otherwise, no issue)

All of this is vastly easier if you can work on and create the USB stick on a Macintosh. See my other guide (for example, the Asrock B660M-HDV guide) for full details; this is a high level overview only. The concepts are all exactly the same.

Run GenSMBIOS to find/generate serials (https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/icelake.html#platforminfo), using MacbookAir9,1 as the SMBIOS of choice, as per the Dortania guide.

Put the EFI in place; use OCAT (https://github.com/ic005k/OCAuxiliaryTools) to help with mounting the EFI partition and similar copy operations.

Works: Video, audio, trackpad, touch, wifi, bluetooth.  As of v1.01: sleep/wake work as expected (a little slow, but it works fine), and after first wakeup, brightness works as expected (ie fully bright screen).  

Doesn't work: One should go into System Settings / Trackpad and unselect "Look up and data detectors", as (at least in 12.5.1) leaving this on caused cursor/trackpad irregularities in Finder. 

Made with help from the Dortania Ice Lake laptop guide, https://github.com/olm3ca/Surface-Laptop-Go (for the Ice Lake i5-1035G1 graphics fix .plist), and https://github.com/Xiashangning/BigSurface (for better trackpad, sleep, power - and your USB mapping must be in place for this work well).  Read all three and become familiar with the information in the articles. 

Tested with:  12.5.1, 12.6.1, 13.01.   

V1.01 Changes: 
1.  Tested very briefly with 12.6.1.  Works great in quick tests.  Note:  airportitwlm.kext DEPENDS ON your OS version.  So if you aren't running 12.x, you MUST change airportitwlm.kext version.  You may wish to keep airportitwlm.kext disabled while you get your OS set up. 
2.  USB Mapping put back in place.  Now sleep/wake works and after sleep, brightness is back and looks good!  Big improvement. 
Overall,  a much better experience.  Get v1.01!  Note that in brief testing with 12.6.1, wake doesn't seem to work.  More testing is required.  Please provide any feedback you can. 

V1.10 Changes: 
1.  Tested briefly with 13.01, Ventura.  airportitwlm.kext for VENTURE is in place; if you run another MacOS, you'll need to adjust this accordingly. 
2.  -igfxblr in NVRAM added (thanks MarblesAreDelicious!) which fixes backlight not working AND sleep not waking due to backlight.  Seems likely sleep doesn't actually turn off the machine; I'm happy with this for now. 
3.  Read #1 again.  To boot this successfully, you'll need either A>Ventura or B>To replace airportitwlm with some other version.  You've been warned!

Find the EFI folder in the RELEASES.  It's a zipfile.  It needs to go onto the EFI partition, in an EFI folder, with OC and BOOT as the two folders under that EFI folder. 
