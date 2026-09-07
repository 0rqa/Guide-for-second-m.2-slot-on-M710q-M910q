
>[!NOTE]
>All information in this repository is provided in good faith but may contain inaccuracies. And I have no liability if you damage your tiny by following this guide 

# Guide-for-second-m.2-slot-on-M710q-M910q

> [!NOTE]
> M710q - the second m.2 slot is only m.2 sata <br>
> M910q - the second m.2 slot is pcie and sata


## Parts sourcing and part placement
The original m.2 slot is M-key 3.2mm -> I used this [one](https://www.aliexpress.com/item/1005004870347795.html). But it's possible to  use for example this one from digikey [MDT420M01002](https://www.digikey.com/en/products/detail/amphenol-icc-fci/MDT420M01002/10232907). Or it's even possible to salvage one from e-waste. I heard that up to 4.2mm ones fits but I haven't tried that.

From SMD parts you will need 8x 0402 100/220nF, 6x 0402 0k (or just solder blob lol), 1x 0402 10k (or two if you are bad at soldering) 

![image1](https://github.com/0rqa/Guide-for-second-m.2-slot-on-M710q-M910q/blob/main/gallery/chipset%20select.JPG)
![image2](https://github.com/0rqa/Guide-for-second-m.2-slot-on-M710q-M910q/blob/main/gallery/pcie%20sata%20side-band.JPG)

## Bios update / re-flashing 

After successfully upgrading the tiny you will have to update the bios. For that you will need USB flash drive formatted in FAT32, and software that can unzip ISOs (I use winrar). 
<br><br>
First thing you will need to do is to [download](https://download.lenovo.com/pccbbs/thinkcentre_bios/m1aj95ausa.iso) the most recent bios ISO image for lenovo tiny4 from lenovo website. If lenovo for some reason made that unavailable there is same [file](https://github.com/0rqa/Guide-for-second-m.2-slot-on-M710q-M910q/blob/main/bios/m1aj95ausa.iso) under bios in this repo.

When you download the ISO, you will want to unzip it and copy all files to FAT32 formatted USB flash drive. After that you will prepare your upgraded tiny by moving jumper next to RJ45 port and COM2 connector from position 5-6 to 1-4. 
<br>
![Image3](https://github.com/0rqa/Guide-for-second-m.2-slot-on-M710q-M910q/blob/main/gallery/bios%20flashing.JPG)

After that you can plug the USB flash drive into second front USB slot from button (actually not sure if necessary, because sometimes it worked when plugged in the back). After that you power up the tiny and the bios updating utility should start on it's own. (DO NOT POWER CYCLE OR REMOVE THE POWER FROM THE DEVICE WHILE UPDATING THE BIOS). When the update finishes put back the jumper from 1-4 to 5-6, after that the second m.2 port should be fully operational. 

## Troubleshooting 

|cause|fix|
|-|-|
|not powering on|some power rail is shorted|
|release of magic smoke|some power rail is shorted but now with possible lasting damages|
|unable to update the bios|try recreating the USB flash drive, or manually flashing my bios with external flasher. Be very aware that you need to make backup of your bios before re-flashing, and that you possible lose the SN and MAC of your original tiny|
|the bios updated but the drive is not in bios or OS| soldering issues|
|the bios updated but drive is not in bios + unable to boot from, but in OS|soldering issues, recommended to check for insufficient connection on m.2 slot or try updating bios again|
|not specified here| You can try contacting me at 0rqa@proton.me|
