# xblue_es-de
ES-DE frontend install scripts for Raspberry Pi OS (CM5)

I Just want to make it easier for everyone to install ES-DE Frontend on top of Raspberry Pi CM5 or Raspberry Pi 5.

This frontend is very nice 😍

[Buy me a coffee](https://buymeacoffee.com/xblue_diy)

![Photo](photo.png)

---------------------------------------------------------------------------------------------------------------------------------

# 1. How to setup

## Install libraries
```bash
sudo apt-get install build-essential clang-format git cmake gettext libharfbuzz-dev libicu-dev libsdl2-dev libavcodec-dev libavfilter-dev libavformat-dev libavutil-dev libfreeimage-dev libfreetype6-dev libgit2-dev libcurl4-openssl-dev libpugixml-dev libasound2-dev libbluetooth-dev libgl1-mesa-dev libpoppler-cpp-dev
```

## Clone the source
```bash
git clone https://gitlab.com/es-de/emulationstation-de.git
cd emulationstation-de
```

## Build the source
```bash
cmake .
make -j8
```

## Install the app
```bash
sudo make install
```

After install, you will see the icon on the system menu. Games > ES-DE

---------------------------------------------------------------------------------------------------------------------------------

# 2. Start up ES-DE frontend on top of Raspberry Pi OS

## Create autostart folder in .config folder
```bash
mkdir ~/.config/autostart
cd ~/.config/autostart
```

## Create es-de.desktop in autostart folder
```bash
nano ~/.config/autostart/es-de.desktop
```

## Paste the below content
```bash
[Desktop Entry]
Type=Application
Name=ES-DE Frontend
Exec=es-de
```

Finally, Press ctrl+o to save file And ctrl+x to exit.

Done! Now you can start ES-DE frontend on top of the desktop.

It will look like you power up the handheld console 😊

Full document of ES-DE Frontend: https://gitlab.com/es-de/emulationstation-de/-/blob/master/INSTALL.md#building-on-unix

---------------------------------------------------------------------------------------------------------------------------------

# 3. Auto rotate the screen 90 degree when play NDS or N3DS

## Create game-start folder under ES-DE folder
```bash
mkdir ~/ES-DE/scripts/game-start
```

## Create game-start-custom.sh file:
```bash
mkdir ~/ES-DE/scripts/game-start/game-start-custom.sh
```

## Paste the content below:
```bash

```

Then Ctrl + o to save file And Ctrl + x to exit.

To rotate the screen back after exit game we need to trigger game-end event.

## Create game-end folder under ES-DE folder
```bash
mkdir ~/ES-DE/scripts/game-end
```

## Create game-start-custom.sh file:
```bash
mkdir ~/ES-DE/scripts/game-end/game-end-custom.sh
```

## Paste the content below:
```bash

```
