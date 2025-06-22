# xblue_es-de
ES-DE frontend install scripts for Raspberry Pi OS CM5

Here is full document of ES-DE Frontend: https://gitlab.com/es-de/emulationstation-de/-/blob/master/INSTALL.md#building-on-unix

I Just want to make it easier for everyone to install ES-DE Frontend on top of Raspberry Pi CM5 or Raspberry Pi 5.

---------------------------------------------------------------------------------------------------------------------------------

# How to setup

## 1. Install libraries
```bash
sudo apt-get install build-essential clang-format git cmake gettext libharfbuzz-dev libicu-dev libsdl2-dev libavcodec-dev libavfilter-dev libavformat-dev libavutil-dev libfreeimage-dev libfreetype6-dev libgit2-dev libcurl4-openssl-dev libpugixml-dev libasound2-dev libbluetooth-dev libgl1-mesa-dev libpoppler-cpp-dev
```

## 2. Clone the source
```bash
git clone https://gitlab.com/es-de/emulationstation-de.git
cd emulationstation-de
```

## 3. Build the source
```bash
cmake .
make -j8
```

## 4. Install the app
```bash
sudo make install
```

After install, you will see the icon on the system menu. Games > ES-DE

---------------------------------------------------------------------------------------------------------------------------------

# Start up ES-DE frontend on top of Raspberry Pi OS



Finally, Press ctrl+o to save file.
