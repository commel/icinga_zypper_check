# Icinga Check for openSUSE's zypper

## Requirements
This check only requires Python 3.6 (openSUSE Leap 15.4 based) and nothing
more. Place it somewhere accessible for Icinga.

## Arguments

	./check_zypper -w10 -c50

* -w triggers a warning for patch + packages update count up from this number
* -c triggers a critical for patch and package count up from this number

Security patches always trigger a critical.

## Installation
Place the zypper_check somewhere where Icinga can access it (e.g. /usr/local/bin). Then append the
content of ```services.conf``` and ```commands.conf``` to your Icinga files.
