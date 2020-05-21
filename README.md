# DEC-PDP-8-on-Arduino-DUE
DEC PDP-8 emulator running FOCAL 69 in 4K for Arduino DUE and better

Ladies and Gentlemen,

The 1960s have called and sent us an AWESOME computer!

This is based on the work of jcw/Jean-Claude, who has made an amazing PDP-8 emulator in 256 lines of C here:

https://git.jeelabs.org/jcw/embello/src/branch/master/explore/1638-pdp8

What you are getting is an ino-file which you just load in the Arduino IDE and flash onto an Arduino DUE (for the complete version), mainly due to the memory requirements. There is also a somewhat reduced version for the Arduino MEGA 2560 - here, I simply "cut off" a few trailing zeroes from the memory dump, so the mem array is SMALLER than 4K, and I am not entirely sure what implications this will have in general, but so far it works. This compromise is needed because the MEGA 2560 has only 8KB SRAM, and a full memory array allocates all of that space to mem[].

Then, once having loaded it, open a terminal emulator of some sort (I am using Picocom on Linux) and ... interact! IN CAPITAL LETTERS ONLY. REMEMBER THIS IS 1969 AND LOWER CASE LETTERS ARE AN UNAFFORDABLE LUXURY ONLY AVAILABLE TO THE WEALTHIEST KINGS OF EUROPE. The built-in Serial Monitor of the Arduino IDE will NOT work, as it will not allow you to terminate lines.

When done, type Ctrl-Backslash to quit. You will see a memory dump. This is in the cleanup()-function, which you may adjust accordingly if you so wish. The idea is, you could perhaps copy and re-use that memory dump in order to initialize the system to your taste and possibly thereby preserve your work, too.

Consider this a quick-and-dirty and highly experimental port - no warranties of its functionality of any kind are given.

You should be able to run any other software, provided it runs on 4K and you get a memory dump of jcw's system, and adjust the starting address accordingly.

Nino Ivanov, 21st May 2020.
