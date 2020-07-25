# brightnessmod

**brightnessmod** is a small script I wrote to view and control my display
brightness (or backlight power level, to be more technical). It interfaces
with the ACPI kernel module for video using the sysfs files (in the `/sys`
directory.

For the user to be able to control the display brightness, they must have
write permission on the backlight device's directory. To see how to do it,
and for more detailed info, please see the relevant [ArchWiki page][1].

Note that the script has not been tested on a multi-monitor setup.

## Usage

View the current brightness percentage:

`backlight`

Set the brightess to 85%:

`backlight =85`

Increase the brightness by 15%:

`backlight +15`

Decrease the brightness by 5%:

`backlight -5`

Disable the minimum-brightness restriction to set the brightness to an
extremely low value **(this may cause the display to go black)**:

`backlight =1 -f`

[1]: https://wiki.archlinux.org/index.php/Backlight#ACPI