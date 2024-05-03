# PulseBlasterUSB-Driver
This is a python wrapper around the SpinApi wrapper used to make working with the PulseBlasterUSB system easier. It optimizes and groups pulse sequences and allows the user to work in a higher level then the sometimes confusing form of the provided wrapper: https://www.spincore.com/support/SpinAPI_Python_Wrapper/Python_Wrapper_Main.shtml.
This was written entirely by me with no affiliation to the Spincore Technologies company.

# Files included
There are only 3 files in this repository. The 1st is a copy of Spincore's provided python wrapper, spinapi.py, which is provided on their website. The 2nd file, PulseBlasterUSB.py, is the custom wrapper around spinapi.py for easier control. This is designed to have a few different ways of controlling the device. To get started with using this, I've included the 3rd document. This document, Driver Instruction.ipynb, is a jupyter-notebook document (should work on jupyter-lab as well) which goes through all functionalities along with examples of them in use. It would be useful to hook the system up to an oscilliscope to visually see the pulses output by the device.

# Needs to Run Program
- You will need to have matplotlib imported on your device, as there is a pulse sequence plotting function.
- You will need to have the spinapi.py wrapper installed such that python can properly utilize it.
- You will need to be sure you have properly installed the SpinAPI backend from Spincore's website, found here: https://www.spincore.com/support/spinapi/

# Getting Started
To get started, I would highly recommend looking at the Driver Introduction.ipynb jupyter-notebook or jupyter-lab document, as I have designed it so that it introduces all functionalities included in the wrapper along with examples that you can observe on an oscilliscope. Note that if you want to observe extremely short pulses, such as 20 ns pulses, you will need to be sure your oscilliscope impedance is not going to cause broadening. One easy fix for this if you have one that has a high impedance is to attach either a 50 Ohm feedthrough terminator to the device or attach a 50 Ohm terminator to a BNC Tee adapter between the input of the oscilliscope channel and the PulseBlasterUSB channel used.

# Caviots
This program default assumes board 0 and clock speed of 500MHz. Some PulseBlasterUSB's use clock's of 100MHz, so please input this accordingly when using these older models. Also note that this has been tested on the model: PulseBlasterESR-PRO-USB-RM2 and, while it should still work for other PulseBlasterUSB models, some of the warning systems built in will be too lenient on older models for things like too short of a pulse. Check the specs of your device to understand the rise time and interval time of your device. This may also work on ESR models, but it hasn't been tested on them properly. I have access to a PulseBlasterESR PCI chip at the moment in the lab I work for that we need to control, so I'm going to test it on this and likely write a seperate GitHub for a PulseBlasterESR driver. When it is finished, I'll link to it here.

# Fair Use
You are free to use this as you wish. While an acknowledgement of this code being used in any product or citation to the github page in any research project would be appreciated, it is not at all required or expected. The only thing I ask is that you don't claim this code is written as your own and if you use it as a base for your own code, that you acknowledge this somewhere in the documentation.

# Contacting me
Feel free to reach out if you run into issues. Keep in mind that I don't personally own this device, so at the time you message me I might not have access to a device to test your issues on. At the moment, you can reach me at erichelgemo@g.ucla.edu.

Good luck with your experiments and I hope this is helpful!
