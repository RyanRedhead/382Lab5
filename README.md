Lab-5
==================
#Purpose

To reverse engineer a remote control using a logic analyzer, interrupts, and the Timer A subsystem.

#Hardware Schematic

The following picture shows the final remote, IR reader with pins , and the MSP430.
![Alt Text](https://github.com/RyanRedhead/382Lab5/blob/master/Hardware.PNG?raw=true)
Connected left from right is Xin, Ground, Power.

#Debugging

Debugging was rahter short for this, my variables did not show up during breakpoints so I had to look into memory to figure it out.

#Testing Methedology/Results

##Day 1

The attached prelab has all of the details for Day 1 activities.

##Day 2

The start file that I added to, showed each decoding of the button pressed under irpacket in the memory.
The first 8 numbers in the irpacket data are the codes for each button press, in this case its the channel + button.
![Alt Text](https://github.com/RyanRedhead/382Lab5/blob/master/Memory.PNG?raw=true)

##Required Functionality

Required functionality was achieved by finding the code for each of the button presses and configuring them to either turn on or turn off a LED.
I sent Dr. York a video of the working required functionality.

The following picture shows what the pulse lengths and codes were for the #3 remote. The volume up/down and channel up/down were from the new remote, there is a significant difference between the two remotes. 
![Alt Text](https://github.com/RyanRedhead/382Lab5/blob/master/Hfiledata.PNG?raw=true)

#Observations/Conclusions

Some observations from this lab include how IR packets are recieved and decoded. Logic 1 pulses are longer and categorized differently which help make up unique 32 bit signatures. Each press does not have the exact pulse lengths so a standard deviation calculated in excel had to be added in.
