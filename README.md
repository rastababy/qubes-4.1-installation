# Qubes-4.1-installation tips
Hello:)
First of all I have to say that Qubes is an amazing system. I hope that the guys of the team never will loose their eagerness to grow up this project for the next decades.
In the next steps I try to show you my setup of Qubes 4.1 with my goal to reach a coloful and easy to use desktop surface. Please never miss that installing software in dom0 may lower your security level, but sometimes a bit more comfort and colors shouldn't be bad and of course everybody have to decide it for themselves. And of course not everything is working perfect at the moment and I am trying to improve it all the time.

But now enough with small talk and let's start with the first steps. I will write it very detailed and hope it helps especially people with less IT experience.
After installing the Qubes 4.1 signed alpha.iso with the following options I enabled the current-testing repo and updated it. I think for the Qubes 4.1 alpha this repo has much more improvements and you need to update from it at least one time to get some useful packages.
            
    sudo qubes-dom0-update --enablerepo=qubes-dom0-current-testing

   Prepare the installation: 
   Create a root account, choose a username, password, storage disks .... everythinglike you prefer it.
   But for me, the only working installing-method in 4.1 is the "automatic". 
   Custom or Blived gui will break the installer, but that maybe only affects my system and you need to test if it is working for you. 
   But my suggestion is like the official documentation to install it on a own SSD without a 2nd partition with Windows on it.Therefore you should use an other.
   
My general installation options:

    make sys-firewall disp    [x]  why not a dispVM? It is always more secure as an other one and that new install feature is working perfect
    make sys-net      disp    [x]  "
    use custom storage pools  [x]  
    use sys-net for both....  [x] ; that makes it easier for me to detect hardware like an integrated webcam or microphone
    create sys-usb            [x] ; take care, that the only plugged in USB-device is the one with the Qubes.is or there can be an error
    create fedora-32 template [x] ; I prefer dom0 based on it & like fedora-32, because it has more and newer .rpm /  packages for office work and customization
    create debian-10 template [x] ; but u can also install debian-11 template later and uncheck this.
    I don't create any other Qubes like personal, work... because I prefer it to do this on my own and based on newer community templates
                
Installing qubes with those settings is much more compatible with my notebook as qubes 3.2x and qubes 4.0x was. But always keep in mind that it is a alpha and this is can be different from the one computer to the other. But my rating definitely is 5/5*.

So before starting with customization I installed some packages and templates I like to use later in dom0 to get more dependencies and files I need to "build" my prefered desktop surface.

               

                         

                         
                         
                         
                        

