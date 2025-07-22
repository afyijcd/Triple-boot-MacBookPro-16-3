Short guide

install MacOS and update

install windows10 through bootcamp

enter windows

update to windows 11

in windows - use diskmanagement to shrink windows partition

download ubuntu T2 (regular ubuntu doesnt work on macbookpro) https://wiki.t2linux.org/

https://github.com/t2linux/T2-Ubuntu/releases/tag/v6.15.6-1

install wifidriver: once you're booted and in your ubuntu desktop, run get-apple-firmware and choose the option "Retrieve the firmware directly from macOS".

Now that all is installed, let's get it cleanup and booted with refind


Disable Secure Boot in Mac Recovery¶

Apple's Secure Boot implementation does not allow booting anything other than macOS or Windows when it is enabled (not even shim signed GRUB). We need to disable it:


  Turn off your Mac

  Turn it on and press and hold Command-R until the black screen flashes 

  Your Mac will boot in the macOS Recovery

  Select your user and enter your password

  Now, from the menu bar choose Utilities > Startup Security Utility

  Enter again the password

  Once in Startup Security Utility:



   set Secure Boot to No Security

set Allow Boot Media to Allow booting from external or removable media



Install refind in ubuntu

    sudo add-apt-repository ppa:rodsmith/refind  
    sudo apt update
    sudo apt install refind




Get windows booting again with gdisk https://wiki.t2linux.org/guides/windows/


Use zip file in this repository, overwrite the contents of /boot/efi/EFI/refind


and voila! nice triple booting macbookpro
