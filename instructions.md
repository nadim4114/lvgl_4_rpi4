# Run LVGL demo on RaspiOS

## Download and flash RaspiOS (on the Host)

https://www.raspberrypi.com/software/

Download the Lite 64-bit version.

Don't forget to specify a username and a password (using the settings tab). It is a good idea to configure your WLAN here too, but you can do it afterward uisng the `raspi-config` tool on the board.  
Once the card is flashed, you can copy the `app-demo` folder into its filesystem, under /home/pi/.


## Copy the config.txt

Copy the `config.txt` in the boot partition of the RPi4. It should already exist, but thw new one configures the display.

## Connect to your board (on the Host)

If using Linux, something like `picocom` or `minicom` is enough to do the monitoring on a PC.  
If using Windows, something like Putty.


## Upgrade your packages (on the RPi4)

```
sudo apt update
sudo apt upgrade
```

## Install missing packages (on the RPi4)

```
sudo apt install git cmake build-essentials
```

## Build the app (on the RPi4)
If you're building the app on the RPi4, it can take 2-3 minutes.

```
cd app-demo

mkdir build
cd build
cmake ..

make -j8
```

Your app can then be found and run at build/src/lvgl_fb.
