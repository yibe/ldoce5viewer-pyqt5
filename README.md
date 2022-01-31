# LDOCE5 Viewer (PyQt5)

This project is ported to PyQt5 which supports retina (HiDPI) display.  

The LDOCE5 Viewer is an alternative dictionary viewer for the Longman Dictionary of Contemporary English 5th Edition (LDOCE 5).

It runs on Linux, Mac OS X and Microsoft Windows.

This software is free and open source software licensed under the terms of GPLv3.

## Installation instructions (Linux, debian based)

You need Python 3 (<=3.7) for the application to work. Python >= 3.8 doesn't work because of a breaking change in it.

Install the required dependencies:

```
sudo apt-get install git make python3 pyqt5-dev-tools python3-pyqt5 python3-pyqt5.qtwebkit python3-lxml python3-whoosh  qtgstreamer-plugins-qt5 python3-distutils python3-sip
```

Download and build:
```
mkdir ~/Programs
cd ~/Programs
git clone https://github.com/purboo/ldoce5viewer-pyqt5.git
cd ldoce5viewer-pyqt5
make
```

Start:
```
python3 ./ldoce5viewer.py
```

`make install` doesn't work as it still tries to use Python 2, which won't work. Instead, you can copy the `ldoce5viewer.desktop` file to `~/.local/share/applications/ldoce5viewer.desktop` and change the `Exec` line to `Exec=python3 /home/<Your Username>/Programs/ldoce5viewer-pyqt5/ldoce5viewer.py` Run `sudo update-desktop-database -q` afterwards and you'll have a menu entry in your desktop environment. 
