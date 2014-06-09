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

##Python3 and virtualenv (virtual environment 3rd party module)
Python 3.3 introduced venv to manage virtual environments and you can visit https://docs.python.org/3/library/venv.html if you would like to use that.

## Virtualenv (not the built in Python3 venv module)
Why you ask? Let's say project1 requires version x.1 of a module and project2 requires version x.2. Using a virtual environement lets you separate the projects and isolate them so that dependencies can easily be managed.
 
#### Install virtualenv
$pip3 install virtualenv

#### Create a new virtual environment (the name of this virtual environment is "venv" without the quotes)
$virtualenv venv

#### Activate the virtualenv named venv
$source venv/bin/activate

#### Using the virtualenv - Python3 is called using python and pip3 is called using pip
(venv)$ 

#### Deactivate the virtual environment exit the virtual environment
$deactivate 
