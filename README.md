Based on the Sofle for Michi board with Via support and modified encoders.

To compile:

- First configure qmk on a conda environment, and specify the folder with `qmk setup -H <path>`. See docs here: https://docs.qmk.fm/#/newbs_getting_started
- Replace /qmk/keyboards/sofle with this repo's `sofle` folder (You can clone the repo anywhere and then create a `ln -s` like this: `lrwxrwxrwx   1 urshulgi urshulgi   46 May  6 21:34 sofle -> /home/urshulgi/github-projects/qmk_sofle/sofle`)
- Now run the command `qmk compile -kb sofle -km via -e CONVERT_TO=michi`
- The compiled .uf2 file will be available inside qmk's folder root as `sofle_rev1_via_michi.uf2`
- In order to install this file, disconnect the USB C cable, then disconnect both halfs of the keyboard, and with one half at a time:
	- Press the reset button under the display, keep it pressed, and plug the keyboard into the PC with USB C
	- An usb drive will appear in the computer; so now drag and drop the uf2 file into the root folder of the flash drive
	- Now the device will reboot itself after its done installing, and the flash drive will disappear. After the keyboard reboots, disconnect from the computer
	- Now repeat with the other half
- After doing this, the keyboard is flashed and the config can be modified with VIA.