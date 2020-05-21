# DEC-PDP-8-on-Arduino-DUE
DEC PDP-8 emulator running FOCAL 69 in 4K for Arduino DUE and better

Ladies and Gentlemen,

The 1960s have called and sent us an AWESOME computer!

This is based on the work of jcw/Jean-Claude, who has made an amazing PDP-8 emulator in 256 lines of C here:

https://git.jeelabs.org/jcw/embello/src/branch/master/explore/1638-pdp8

What you are getting is an ino-file which you just load in the Arduino IDE and flash onto an Arduino DUE (at least), mainly due to the memory requirements.

Then, once having loaded it, open a terminal emulator of some sort (I am using Picocom on Linux) and ... interact! The built-in Serial Monitor of the Arduino IDE will NOT work, as it will not allow you to terminate lines.

When done, type Ctrl-Backslash to quit. You will see a memory dump. This is in the cleanup()-function, which you may adjust accordingly if you so wish. The idea is, you could perhaps copy and re-use that memory dump in order to initialize the system to your taste and possibly thereby preserve your work, too.

Consider this a quick-and-dirty and highly experimental port - no warranties of its functionality of any kind are given.

You should be able to run any other software, provided it runs on 4K and you get a memory dump of jcw's system, and adjust the starting address accordingly.

Nino Ivanov, 21st May 2020.
