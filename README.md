# sdshrink
How to shrink a Raspbian SD card

Software needed:
- [GPT fdisk](https://sourceforge.net/projects/gptfdisk/)
- [dd for windows](http://www.chrysocome.net/dd)
- [PARAGON Partition Manager Free](https://www.paragon-software.com/free/pm-express/)

01. Insert the SD card in your computer and open PARAGON Partition Manager Free.
02. Select "Partition Manager".

![alt text](https://github.com/aristosv/sdshrink/blob/master/step1.png)

03. Select the right edge of your SD card, and drag it all the way to the left.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step2.png)

04. A popup will show you the minimum size you can shrink the SD.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step3.png)

05. Modify that number so you add some free space to the partition and click "OK"

![alt text](https://github.com/aristosv/sdshrink/blob/master/step4.png)

06. Click "Apply" and then "Yes"

![alt text](https://github.com/aristosv/sdshrink/blob/master/step5.png)

07. This will take a few minutes depending on the size of the SD.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step6.png)

08. You will be notified when the process is finished.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step7.png)

09. This is exactly how you want the SD to be. Shrunk down with some free space. The rest of the SD is unallocated.

![alt text](https://github.com/aristosv/sdshrink/blob/master/step8.png)

10. Open [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/files/latest/download) and create an image of the SD. Its size will be the full size of your SD (eg. 16GB)

![alt text](https://github.com/aristosv/sdshrink/blob/master/step9.png)
