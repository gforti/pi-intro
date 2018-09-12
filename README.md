# Intro Raspberry PI with Node.js

## What do you need?

I recommend to get the `CanaKit Raspberry Pi 3 B+ (B Plus) Ultimate Starter Kit` which features everything you need to get started
The kit can be found on amazon for about $89.99 

- Raspberry Pi 3 B+
- Micro SD Card (Class 10) pre-loaded with NOOBS
-- https://www.raspberrypi.org/downloads/raspbian/
- 2.5A Power Supply with 5 feet Micro USB Cable
- HDMI Cable
- Large Breadboard
- Jumper Wires
- 1 LED any color (Blue/Red/Yellow/Green)
- Resistors 
- 1 Push Button Switch
- Screen display(TV/Monitor) with HDMI input
- USB keyboard and mouse

## OS Installation

The raspberry pi will run the OS from the SD card. With NOOBS pre-installed it will be much easier to install
raspbian.  if you buy the SD card pre-configured, Setup wi-fi so the lastest version can be installed.

> Vist https://www.raspberrypi.org/downloads/raspbian/

## Configuration

Depending if the OS was installed or the lite version was installed you will still need to configure a few things.

- Consider updating the hostname and password
- Update the time zone/ localisation (This can affect the keyboard settings if country is not US)
- Configure Wi-Fi

Once installed you should be able to install node.js(linux).  


## Terminal commands 

```sh
$ sudo npm install --unsafe-perm
```

## Issues with NPM install

```sh
$ sudo npm rebuild
```

## Stop the App
```sh
$ ctrl + c
```

## Shutdown PI
```sh
$ sudo shutdown -h now
```

## Restart PI
```sh
$ sudo shutdown -r now
```

## Remove Folder
```sh
$ sudo rm -rf [folder-name]
```

## Clone GIT Repo
```sh
$ git clone https://github.com/...
```

## check directory
```sh
$ ls
```

## change directory
```sh
$ cd ..
```


## update wifi password settings
```sh
$ sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
```

Then add the following.  The higher priority number will try to connect first.

```js
network={
    ssid="testing"
    psk="password"
    priority=2
    id_str="work"
}
```

## restart wifi

```sh
$ /etc/init.d/networking restart
```


## check ip address
```sh
$ hostname -I
```

## check wifi name
```sh
$ iwgetid
```

## SSH in
```sh
$ ssh pi@<IP> [-port 22 ]
```


## lessons

- Need resistors


# understanding pins

VCC - 5v
gnd - ground
do - GPIO pin digital output
ao - analog output

ground (GND) = -
VCC (3.3v or 5v) = +


## Running the App

 Note that everyone must be on the same network/WiFi. `Chrome` is the recommend web browser.

> `Will run on `http://[ip_address]:3000/` 
