---
layout: post
title: 'TIL: BlueZ 5 Compatability issue with SDP on Debian'
date: '2016-05-15 08:27'
---

**All lines count does not include empty-line**

To those who are enjoying system.d, take a look at this excellent [so answer](http://stackoverflow.com/questions/33110992/python-code-for-bluetooth-throws-error-after-i-had-to-reset-the-adapter)

Now for those who're using init.d scripts, the solution is the same: enabling bluetoothd service to run with a --compat or -C flag. The step is slightly different.

init.d scripts are located inside `/etc/init.d`. `cd` there, then `sudo` with your text editor to edit the `bluetooth` file. On my end, thats' `sudo vi bluetooth`

The startup script is fairly clear in what it is trying to do. Focus on the switch-case statement by the end of the script, and look at the `start` case. The first line log what it does, the next 6 test if the service is already on. Now on the 7th line, you should see something like this:

`start-stop-daemon --start --background $SSD_OPTIONS`

Just add the `-C` flag like so:

`start-stop-daemon --start --background $SSD_OPTIONS -C`

And we are all good. The reason the flag are added in that specific spot is because this bluetooth script is using variable across commands. Thus changing the variables will affect other command where such variable makes zero sense.

`sdp browse local` should now _run_ as expected.
