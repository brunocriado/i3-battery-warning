i3-battery-warning
==================


This is a simple battery warning script. It uses i3's nagbar to display warnings.

Let this script run as a cronjob.

Open your crontab.

$ crontab -e

Add the following line to check battery status every minute

*/1 * * * * env DISPLAY=:0 /PATH/TO/YOUR/SCRIPT/i3batwarn.sh

in the cron tab (before calling this script).

screenshot
==========

![ScreenShot](screenshot.png)

fork changes (Bruno Criado)
===========================
I usually use my web browser and terminal in fullscreen, so I've added i3-msg to disable fullscreen and show the
warning.

fork changes
============

Added a pidfile where the pid of each (one max) nagbar is saved
and a check to kill the nagbar if the battery is above the limit.
This usually works but sometimes the nagbar has to be closed manually.
