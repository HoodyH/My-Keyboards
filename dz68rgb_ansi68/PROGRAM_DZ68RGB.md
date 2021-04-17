# DZ65RGB v1

## Configure and build the firmware
https://config.qmk.fm/#/dztech/dz65rgb/LAYOUT_65_ansi  
Compile your keymap, click load default, wait for you to edit it, click compile, then click firmware to download your bin file

## Zadig
Install zadig https://zadig.akeo.ie/

Zadig stuff is not really neaded, try without it.
Open the zadig and install the dfu driver

## Qmktoolbox
install qmktoolbox https://github.com/qmk/qmk_toolbox/releases

### Enter programming mode
To activate the BootLoader mode, use one of this two:
- Press and hold esc then connect to USB
- Behind spacebar, set the switch to BL mode, then connect to USB

## Upload firmware Windows
Via qmktoolbox set the following configs
- **Keyboard:** dztech/dz65rgb/v1 keyboard
- **Microcontroller:** atmega32u4
- **Keymap:** None

## Upload firmware Ubuntu
sudo dfu-util -a 0 -d 0483:df11 -s 0x08000000:leave -D firmware.bin
