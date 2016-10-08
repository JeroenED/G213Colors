# G213Colors
A script to change the key colors on a Logitech G213 Prodigy Gaming Keyboard.

## What it does
G213Colors lets you set the color(s) and certain effects of the illuminated keys on a G213 keyboard.

Since Logitech is mostly ignoring the Linux market with their "Gaming Software" but i wanted to use my expensive new keyboard under linux also without tolerating the color cycling animation all the time i decided to reverse engineer their USB protocol and to write my own script to control the keyboard. 
Also my keyboard is attached to an Aten KVM switch which interferes with the Logitech software to the degree that the computer becomes unusable in the worst case and the software does not start in the best case.

G213Colors was built and tested as a Python script under Linux for the G213 keyboard specifically, but it could potentially be run under other OS'es and used for other Logitech keyboards as well, after some adaptation. 
Please understand that i do not support any such adaptation, if you want to do it on your own **you are on your own**.

The "Wave" color effect that is available with the Logitech software could not be replicated since it is completely generated in the software by updating the colors every x ms (In contrast to the other effects which run on they keyboard itself). You could generate this effect with a script, but since the script has to detach the kernel driver from one of the G213's interfaces the multimedia keys would most likely stop working. Unfortunately this is a side effect of the linux driver structure.

## Installation
TBD

## Usage
G213Colors needs to be run as root as long as you didn't add your own user as a privileged user for that USB device.

G213Colors is designed to be used as a shell script for maximum flexibilty and the syntax is easy and Bash-like.
For help on how to use G213Colors call the program without any arguments:

`sudo python G213Colors.py`

## Changelog
Changelog v0.1:
* Initial checkin
