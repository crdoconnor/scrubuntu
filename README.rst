Scrubuntu
=========

Scrubuntu is an ansible playbook for scrubbing the crap from a stock ubuntu server installation.

Stuff like apache, sendmail, CUPS and X11 has no business being preinstalled on a bare bones
internet facing server, but most ubuntu images still have them. Same for chef, puppet, samba, etc.

This playbook purges all of it leaving you a clean, fresh server ready to install the packages
that you actually want.

It also:

* Fixes a common locale issue on stock ubuntu server images that spews errors every time you apt-get install something.
* Updates and upgrades everything.

After running it
================

Run this::

$ dpkg -l | grep ^i

If there is anything still in the list that you think shouldn't be, please drop me a mail or fork and
add to the list of packages to purge.
