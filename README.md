# xblue_es-de
ES-DE frontend install scripts for Raspberry Pi OS (CM5)

I Just want to make it easier for everyone to install ES-DE Frontend on top of Raspberry Pi CM5 or Raspberry Pi 5.
This frontend is very nice 😍

![Photo](photo.png)

---------------------------------------------------------------------------------------------------------------------------------

# How to setup

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

# Start up ES-DE frontend on top of Raspberry Pi OS

## Create autostart folder in .config folder
```bash
mkdir ~/.config/autostart
cd ~/.config/autostart
```

## Create autostart folder in .config folder
```bash
nano ~/.config/autostart/es-de.desktop
```

## Paste the content below
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
