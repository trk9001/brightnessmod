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

**Note:** To invoke the script by name solely, give it executability using
`chmod u+x brightnessmod` and put it in `$HOME/bin` or `/usr/local/bin`.
Also make sure you have Python 3 installed.

View the current brightness percentage:

`$ brightnessmod`

Set the brightess to 85%:

`$ brightnessmod =85`

Increase the brightness by 15%:

`$ brightnessmod +15`

Decrease the brightness by 5%:

`$ brightnessmod -5`

Disable the minimum-brightness restriction to set the brightness to an
extremely low value **(this may cause the display to go black)**:

`$ brightnessmod =1 -f`

Specify which backlight interface to use:

`$ brightnessmod --interface intel_backlight`

[1]: https://wiki.archlinux.org/index.php/Backlight#ACPI
