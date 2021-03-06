# sdshrink
How to shrink a Raspbian SD card

Software needed:
- [GPT fdisk](https://sourceforge.net/projects/gptfdisk/)
- [dd for windows](http://www.chrysocome.net/dd)
- [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/files/latest/download)
- [PARAGON Partition Manager Free](https://www.paragon-software.com/free/pm-express/)

01. Insert the SD card in your computer, open PARAGON Partition Manager Free and select "Partition Manager"

![alt text](https://github.com/aristosv/sdshrink/blob/master/step01.png)

02. Select the right edge of your SD card, and drag it all the way to the left.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step02.png)

03. A popup will show you the minimum size you can shrink the SD.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step03.png)

04. Modify that number so you add some free space to the partition and click "OK"

![alt text](https://github.com/aristosv/sdshrink/blob/master/step04.png)

05. Click "Apply" and then "Yes"

![alt text](https://github.com/aristosv/sdshrink/blob/master/step05.png)

06. This will take a few minutes depending on the size of the SD.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step06.png)

07. You will be notified when the process is finished.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step07.png)

08. This is exactly how you want the SD to be. Shrunk down with some free space. The rest of the SD is unallocated.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step08.png)

09. Open Win32 Disk Imager and create an image of the SD. Its size will be the full size of your SD (eg. 16GB)

![alt text](https://github.com/aristosv/sdshrink/blob/master/step09.png)

10. Run "gdisk64.exe -l big_image.img" and write down the "End" sector of the "Linux filesystem" partition.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step10.png)

11. Run "ddrelease64.exe --progress if="big_image.img" of="small_image.img" bs=512 count=**3665919**".

![alt text](https://github.com/aristosv/sdshrink/blob/master/step11.png)

12. Notice the size difference after shrinking the image.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step12.png)

There you go! :)
