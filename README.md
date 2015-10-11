# Python Serial Monitor

## Installation

### Ubuntu
It is likely that the required pySerial library is already installed. If not, you can install by running the following commands.
```bash
sudo apt-get install python-pip
pip install pyserial
```

### OSX
```bash
wget https://bootstrap.pypa.io/get-pip.py
python get-pip.py
```
You may need to run `sudo python get-pip.py` if you get a permission denied error.

### Windows
At the moment, I haven't been able to get this to run inside of a Cygwin terminal. Use a standard windows Command Prompt.

If you don't have Python 2.7 installed, you will need to install it from https://www.python.org/downloads/. Run the exe to install Python 2.7.x and make sure to turn on the option to add Python to your path during the installation. If you miss this step, you will need to manually add Python to your path.

Download get-pip.py from https://bootstrap.pypa.io/get-pip.py. In a Command Prompt, navigate to the directory you downloaded get-pip.py to and run `python get-pip.py`.

Run `pip install pyserial`.

## Use

After following the installation instructions, use Python Serial Monitor by running `python python-serial-monitor.py` in the directory that you downloaded the python script to. If your Teensy is connected and is running some code where serial communication has been setup, it should find the correct port and connect automatically. Pressing 'esc' should exit the program (ctrl+c or cmd+c won't work).

Note: Python Serial Monitor will search for the port at which your Teensy is connected. To do this, it trials the following options where 'n' is a number ranging from 0 to 64.

```bash
'/dev/ttyUSBn',
'/dev/ttyACMn',
'COMn',
'/dev/tty.usbmodem1234n'
```

If your Teensy is connected to a different port base name (specifically Mac OSX users), you will need to add the base name inside python-serial-monitor.py manually.
