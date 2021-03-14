# Qubes-4.1-desktop-customization
Hello:)
First of all I have to say that Qubes is an amazing system. I hope that the guys of the team never will loose their eagerness to grow up this project for the next decades.
In the next steps I try to show you my setup of Qubes 4.1 with my goal to reach a coloful and easy to use desktop surface. Please never miss that installing software in dom0 may lower your security level, but sometimes a bit more comfort and colors shouldn't be bad and of course everybody have to decide it for themselves. And of course not everything is working perfect at the moment and I am trying to improve it all the time.

But now enough with small talk and let's start with the first step.
After installing the Qubes 4.1 signed alpha iso with the following options I enabled the current-testing repo and updated it.

    Prepare the installation: Create a root account, choose a username, password, storage disks .... like you prefer it.
    For me, the only installing-method in 4.1 is to use the automatic installation. Custom or Blived gui will break the installer, but that maybe only affects my system and you need to test if it is working for you, but I suggest to install Qubes on a own SSD without a Windows partition or anything.
   
My installation options: make sys-firewall disp   [x]  why not a dispVM is always more secure as an other one and that new install feature is working perfect
                         make sys-net      disp   [x]  "
                         use custom storage pools [x]  
                         use sys-net for both.... [x]  that makes it easier for me to detect hardware like your integrated webcam or microphone
                         create sys-usb           [x]  becareful that the only usb stick insert is that with the Qubes.iso - otherwise it could be a error at create
                         
                         These are the main changes I did at the installation progress. 
                         
                         
                         
                        

