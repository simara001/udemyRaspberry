### Installing Raspbian

It is expected that your *SD Card* has installed a version for your Raspberry Pi. In case you have some problem, you might be able tod download it from [here](http://www.raspberrypi.org/downloads/). The process of formatting your **SD Card** is more complex than simply copy-paste a file. The instructions to do it can change depending on the OS you are using. My prefer OS is the Mac OS X (Currently Mavericks) and here are the instructions.

#### Installing Raspbian from Mac OS X

+ You will need to open your `Terminal`
+ Put `df -h`
+ As a result you will see all the disks mounted on your computer
+ Insert the Card
+ Put `df -` again
+ You are looking for a disk that was not mounted before (i.e. `/dev/dis3s2`)
+ Unmount the card by typing `sudo diskutil unmount /dev/disk3s2` (don't try to do it using **Finder** or **Disk Utility**)
+ Get the raw device name by changing *disk* for *rdisk*, and removing the *s2* part (i.e. `/dev/disk3s1` for `/dev/rdisk3`)
+ Unzip the file you have downloaded from *Raspberry Downloads*
+ Substitute your raw device info in the next code: `sudo dd bs=1m if=~/2012-09-18-wheezy-raspbian.img of=/dev/rdisk3`
+ After a couple of minutes everything is ready :)