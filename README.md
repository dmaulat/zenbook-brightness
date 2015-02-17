# zenbook-brightness
A little script for Debian/Ubuntu to bind the brightness control to keypress on ASUS Zenbook 303LA with Intel Graphics HD 5500.

## Basic usage

Increase brightness:

    $ sudo bash backlight -u
    
Decrease brightness:
    
    $ sudo bash backlight -d

## Installation

1. Copy this script to /usr/bin/backlight:

    `$ sudo mv backlight /usr/bin/backlight`

2. Allow sudo call to this script without a password:

    * open the sudoers file 
    
        `$ sudo visudo`
    
    * Add the following line, replacing `username` with your username
    
        `username ALL=(ALL) NOPASSWD: /usr/bin/backlight`
    
3. Go to System Settings > Keyboard > Shortcuts > Custom Shortcuts

4. Add these two shortcuts: 
    
    Name: `Brightness up`
    Command: `sudo backlight -u`

    Name: `Brightness down`
    Command: `sudo backlight -d`
    
5. Map them e.g. to Ctrl+F5 and Ctrl+F6

## Adaptation

Fell free to change the value `STEP` in the script. On my Zenbook LA303, the brightness values range from 0 to 928. 

## Inspiration

Inspired by https://github.com/arunvelsriram/BrightnessControl.

## Tested configuration

Asus Zenbook 303LA with Ubuntu 14.10 64bits.
