# Icinga Check for openSUSE's zypper

## Requirements
This check only requires Python 3.6 (openSUSE Leap 15.4 based) and nothing
more. Place it somewhere accessible for Icinga.

## Arguments

	./check_zypper -pack_w 10 -pack_c 50 -patch_w 5 -patch_c 10

* -pack_w triggers a warning for packages update count up from this number
* -pack_c triggers a critical for patch and package count up from this number
* -patch_w does the same for patches (not security)
* -patch_c does the same for patches (not security)

Any security patches will always trigger a critical.

All parameters are optional.

## Installation
Place the zypper_check somewhere where Icinga can access it (e.g. /usr/local/bin). Then append the
content of ```services.conf``` and ```commands.conf``` to your Icinga files.
