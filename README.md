# Wiping and Booting the Raspberry Pi

This mark down will teach you how to wipe and boot you raspberry pi by following these steps.

1) Take your SD card and plug it in to your computer. 
2) Go to you terminal, and type the following lines of code:

```
sudo diskutil partitionDisk /dev/disk2 1 MBR "Free Space" "%noformat%" 100%
```
This will start to partition disk2 (the SD card). The name of the disk may vary depending on you computer.

3) Run the following lines of code in your terminal:

```
sudo dd bs=1m if=/Users/(username)/Downloads/2015-05-05-raspbian-wheezy.img  of=/dev/rdisk2
```
4) Eject the SD card.

5) Plug in the SD card into your Raspberry Pi.
    
    Username: pi
    Password: raspberry
    
6) Keep in mind that the spelling is RASPBERRY, with a p. I spent a numerous amount of hours trying to figure out why this whole process didn't work.


