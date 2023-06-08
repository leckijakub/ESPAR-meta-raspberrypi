sudo umount /dev/sda*
sudo bmaptool copy --bmap core-image-base-raspberrypi0-wifi.wic.bmap core-image-base-raspberrypi0-wifi.wic.bz2 /dev/sda
sudo umount /dev/sda*

sudo cp core-image-base-swu-raspberrypi0-wifi.swu /media/jale/data/
sudo umount /dev/sda*

swupdate -e "raspberrypi0-wifi,mmcblk0p3" -i /data/core-image-base-swu-raspberrypi0-wifi.swu -v
