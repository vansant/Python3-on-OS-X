Python3-on-OS-X
===============

Installing Python3 on OS X Mavericks

##Download Python3
Visit https://www.python.org/downloads/ to get the most recent version of the Python3. At the time of this writing it is version 3.4.1 and the OS X download is named python-3.4.1-macosx10.6.dmg.

##Python3 Installation - Standard
Open python-3.4.1-macosx10.6.dmg and double click on Python.mpkg and follow the on screen instructions.

##Python3 Installation - Without Admin Rights

###Compile Python3 from source code to ~/Python-3.x.x

Download the latest version of Python3 source code from https://www.python.org/downloads/source/. At the time of this writing it is version 3.4.1.

Run in terminal:
* $cd ~/Desktop
* $curl https://www.python.org/ftp/python/3.4.1/Python-3.4.1.tgz | tar zx
* $mkdir ~/Python-3.4.1
* $cd Python-3.4.1/
* $./configure --prefix=/Users/$USER/Python-3.4.1
* $make; make install
* $rm -rf ~/Desktop/Python3.4.1

### Add Python3 to $PATH
Run in terminal:
* $nano ~/.bash_profile
* Add the following export statment
* export PATH=/Users/$USER/Python-3.4.1/bin:$PATH
* Close and reopen terminal to use python3.4 command from terminal
