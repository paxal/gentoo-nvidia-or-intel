gentoo-nvidia-or-intel
======================

Gentoo init script to select right X.org configuration and load correct display driver

How it works ?
--------------

Some laptops have nVidia Cards with Optimus technology.

* When Optimus is enabled, the main video device of the laptop is an intel device.
* When Optimus is disabled, the main video device of the laptop is an nVidia device.

This script can automatically switch your configuration to select the correct video driver.

* It checks if Optimus is enabled
* It selects the right module : intel or nvidia (or nouveau if nvidia is not installed)
* It will select the correct OpenGL implementation (xorg or nvidia)

Installation
------------

Clone the repository

    git clone https://github.com/paxal/gentoo-nvidia-or-intel.git

Copy files into your system /etc and enable the script at init :

    rc-update add nvidia-or-intel default

Configuration
-------------

You can modify the X11 configuration files to match your needs.
