
>[!NOTE]
>All information in this repository is provided in good faith but may contain inaccuracies.

# Guide-for-second-m.2-slot-on-M710q-M910q

> [!NOTE]
> M710q - the second m.2 slot is only m.2 sata <br>
> M910q - the second m.2 slot is only pcie


## Parts sourcing and part placement
The original m.2 slot is M-key 3.2mm -> I used this [one](https://www.aliexpress.com/item/1005004870347795.html). But it's possible to  use one from digikey like [MDT420M01002](https://www.digikey.com/en/products/detail/amphenol-icc-fci/MDT420M01002/10232907). Or its even possible to salvage one from e-waste. I heard that even 4.2mm one fits but I haven't tried.

For SMD parts you will need 8x 0402 100/220nF, 6x 0402 0k (or just solder blob lol), 1x 0402 10k (or two if you are bad at soldering) 

![image1](https://github.com/0rqa/Guide-for-second-m.2-slot-on-M710q-M910q/blob/main/gallery/chipset%20select.JPG)
![image2](https://github.com/0rqa/Guide-for-second-m.2-slot-on-M710q-M910q/blob/main/gallery/pcie%20sata%20side-band.JPG)

## Bios update / re-flashing 

After successfully upgrading the tiny you will have to update the bios. For that you will need USB flash drive formatted in FAT32, and software that can unzip iso (I use winrar). <br>
First thing you will need to do is to [download](https://download.lenovo.com/pccbbs/thinkcentre_bios/m1aj95ausa.iso) the most recent bios ISO image for lenovo tiny4 from lenovo website. If lenovo for some reason made that unavailable there is same [file]() under bios in this repo.

