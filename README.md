spin.off
========

[![GPLv3](http://img.shields.io/badge/license-GPLv3-blue.png)](https://github.com/153957/spin.off/blob/master/LICENSE)
[![Travis Status](http://img.shields.io/travis/153957/spin.off/master.png)](https://travis-ci.org/153957/spin.off)

This is the website for the
[spin.off](http://www.spinoff.me).


Installing cactus
-----------------

This site uses [Cactus](https://github.com/eudicots/Cactus) to build.

Cactus is a Python program, so Python 2.7 is required.
Also pip is used to install cactus.
Other packages that are required by cactus are automatically installed.
So open a Terminal and run:

    pip install cactus

If all goes well cactus can now be used.

To start a local webserver navigate to the repository in the Terminal
and run:

    cactus serve

You can then point your browser to http://127.0.0.1:8000 to view the
local version. If you make any changes to the code this should be
reflected almost immediently in the local website.


Synchronize
-----------

To update the live server use these commands:

    cd [path to repository]
    rm -rf .build
    cactus build
    rsync -avz .build/ [username]@[server address]:[path to web root]
