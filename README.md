Choose Hive
===========

Tired of logging into a hive machine and seeing this?

```
 17:26:05 up 6 days,  3:47, 17 users,  load average: 12.90, 12.54, 11.56
USER     TTY      FROM              LOGIN@   IDLE   JCPU   PCPU WHAT
cs61c-au pts/1    airbears2-10-142 15:32    1:22m  0.24s  0.24s -bash
cs61c-jp pts/3    c-24-6-6-54.hsd1 16:33   52:57   0.21s  0.21s -bash
cs61c-au pts/6    airbears2-10-142 16:11    1:13m  0.24s  0.24s -bash
cs61c-hn tty7                      Mon10    6days  6:07   1.31s gnome-session --session=ubuntu
cs61c-ax pts/8    mar-115-195.resh 17:22    2:53   0.30s  0.30s -bash
cs61as   pts/10   airbears-136-152 16:40   32:13   0.29s  0.29s -bash
cs61c-jp pts/12   c-24-6-6-54.hsd1 16:44   36:13   0.32s  0.32s -bash
cs61c-aw pts/13   c-50-174-26-19.h Wed16   25:08m  0.28s  0.28s -bash
cs61c-hn pts/2    :0               Mon11    3days  0.02s  0.02s bash
cs61c-aq tty8                      Mon18    6days 11:16   1.24s gnome-session --session=ubuntu
cs61c-au pts/7    :3.0             16:18    1:06m  0.02s  0.02s bash
cs61c-aq pts/0    :1               Mon18    2days  6:35   0.07s bash
cs61c-as tty9                      Wed18    6days 20:29   0.57s gnome-session --session=ubuntu
cs61c-au pts/9    :3.0             16:15    1:10m  8:59m  0.02s bash
cs61c-au pts/11   :3.0             16:42   43:15  59.50s 59.49s java -jar /home/ff/cs61c/bin/Mars.jar
cs61c-au tty10                     16:13    6days  2:06   0.13s gnome-session --session=ubuntu
cs194-ap pts/1    c-24-130-184-210 17:44    0.00s  0.13s  0.00s w
```

This was hive2.  Meanwhile hive7 looked like this:

```
 17:30:14 up 23:15,  1 user,  load average: 0.00, 0.02, 0.05
USER     TTY      FROM              LOGIN@   IDLE   JCPU   PCPU WHAT
cs194-ap pts/1    c-24-130-184-210 17:44    0.00s  0.13s  0.00s w
```

Yeah that's right, all to myself.

Use this script to get yourself onto the hive machine with the least active connections.


Setup and Usage
=====

* Make sure you have a private/public keypair and put your public key in `~/.ssh/authorized_keys` on any hive machine. Keep your private key private (this goes without saying)
* Use `ssh-add` to add your private key to your ssh agent
* Clone the repo: `git clone https://github.com/nherson/choose-hive`
* Edit the variables in the top of the script, filling them in as necessary
* Run `./choose-hive`, and you're done. It'll find the best hive and login
* (optional) Add the location of `choose-hive` to your path


TODO
=====
* Add options like `-u` for `USER` and `-i` for the path to a private key
* Add support for second floor Soda machines
* Support for a config file to source
* Create an install script to make `$PREFIX/bin` and place the `choose-hive` script there

Contributing
=======
Think this is nifty? Submit a pull request to help make it better!  This script was only tested on OSX.  If you run Linux and something breaks, let me know so that I can fix it.
