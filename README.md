# Creating a bootable SD card for the Raspberry Pi

This README will show you how to create a bootable SD card for your Raspberry Pi. 

1) Download the wheezy image from the Raspberry download page [here].

2) Take your SD card and plug it in to your computer. 

3) Note down the disk number of your SD card. On my Mac it  was /dev/disk2 but yours might be different. 

** This is very important. You could wipe out your hard drive if you make a mistake here ** 

2) Go to you terminal, and type the following lines of code. This will start to partition disk2 (the SD card). The name of the disk may vary depending on you computer.

```
sudo diskutil partitionDisk /dev/disk2 1 MBR "Free Space" "%noformat%" 100%
```

3) Run the following lines of code in your terminal. It will copy your image to your SD card. Note that the disk name is rdisk instead of disk.

```
sudo dd bs=1m if=/Users/(username)/Downloads/2015-05-05-raspbian-wheezy.img  of=/dev/rdisk2
```

4) Eject the SD card.

5) Plug in the SD card into your Raspberry Pi.
    
    Username: pi
    Password: raspberry
    
6) Keep in mind that the spelling is "raspberry", with a p. I spent a hours trying to figure out why this whole process didn't work.

[here]:https://www.raspberrypi.org/downloads/
