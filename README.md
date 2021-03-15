# Qubes-4.1-installation tips for beginners
Hello:)
First of all I have to say that Qubes is an amazing system. I hope that the guys of the team never will loose their eagerness to grow up this project for the next decades.
In the next steps I try to show you my setup of Qubes 4.1 with my goal to reach a coloful and easy to use desktop surface. Please never miss that installing software in dom0 may lower your security level, but sometimes a bit more comfort and colors shouldn't be bad and of course everybody have to decide it for themselves. And of course not everything is working perfect at the moment and I am trying to improve it all the time.

But now enough with small talk and let's start with the first steps. I will write it very detailed and hope it helps especially people with less IT experience.
After installing the Qubes 4.1 signed alpha.iso with the following options I enabled the current-testing repo and updated it. I think for the Qubes 4.1 alpha this repo has much more improvements and you need to update from it at least one time to get some useful packages.
            
    sudo qubes-dom0-update --enablerepo=qubes-dom0-current-testing

   Prepare the installation: 
   Create a root account, choose a username, password, storage disks .... everything like you prefer it.
   But attention! For me, the only working installing-method in 4.1 is the "automatic". 
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

So before starting with customization I installed some packages in dom0 to get more dependencies and files I need to "build" my prefered desktop surface and the templates I like to use later, especially the Kali -template from fepitre ,because later, there is not enough root space to extract it & you need to increase the root space to install this. This step can be safed on this way, but it is not a real problem to increase it later An easy way is to use the KDE partition manager and install it in dom0. Then you can change the root volume in a gui and do some other changes at your partitions, too if you wanna it.

Now let us start to install some more dependencies for riching your system, to build packages later and just for better running and compatibility.
You have to run the sudo qubes-dom0-update command after every "\" line.

    sudo qubes-dom0-update gcc-c++ meson \
      cairo-devel cmake automake xcb-util-devel libxcb-devel xcb-proto dbus-devel \
      xcb-util-image-devel wireless-tools-devel libnl3-devel xcb-util-wm-devel \
      flex bison libxkbcommon-devel libxkbcommon-x11-devel pango-devel startup-notification-devel librsvg2-devel \
      libXcomposite-devel libXrandr-devel libXinerama-devel libconfig-devel asciidoc imlib2-devel \
      xcb-util-keysyms xcb-util-keysyms-devel xcb-util-renderutil xcb-util-renderutil-devel \
      libev libev-devel uthash-devel asciidoc libevdev libevdev-devel libevdev-utils \
      libXrender libXrender-devel libmpdclient libmpdclient-devel \
      gcc kmod grub2-tools perl-bignum make    #this line is for building a nvidia driver later/ radeon users don't need it
      
   
And now finally I installed KDE and we can start with the customization, because then you don't need to order your icons and such things twice.
Not everybody prefers KDE instead of Xfce as a desktop and of course you can use Xfce, i3 or whatever you like but I think KDE is one of the easiest to use, especially for the people with less Linux experience and you can style it better as the other. An other point is that I am using KDE for years and I don't now much about Xfce, but be free to choose what you want.
If you like KDE it is a good possibility for qubes 4.1 and the perfomance & compatibility is great as well. One more advantage of KDE is that you can change the languages and make qubes available in your foreign language. So, if you like KDE, too you can take a look at my sytle tips at the other page and go on here with installing it and all its dependencies to run smooth.

Now let us install the KDE-Desktop instead of the Xfce, running  a terminal in dom0 and install:

    1. sudo qubes-dom0-update @kde-desktop-qubes ; here you will get an error that the group is not available, but we will install the the complete packages now!
    2. sudo dnf install plasma-workspace   ; this will install the main surface and after installing you can logout from Xfce and switch to KDE

But to get some nice widgets working in KDE we need to install some more dependencies.
 
    3. sudo qubes-dom0-update        qt5-qtbase-devel qt5-qtdeclarative-devel qt5-qtx11extras-devel  \
             "                       kf5-plasma-devel kf5-kglobalaccel-devel kf5-kxmlgui-devel kscreen  ;from now you can install a widget like virtual desktopbar

Next I installed some more packages that are usually available at KDE, like the file manager, console, screen tools and such things.  

    4. sudo qubes-dom0-update        kscreen dolphin konsole 
                                    
                                    
                                    
                                    



 

               

                         

                         
                         
                         
                        

