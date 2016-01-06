# Power supply

Users have two options to supply power to Phenox2, using battery or external supply cable.

# Basic
The circuit board of Phenox2 is not protected. So it can be easily broken when it touches to other metal stuff. (A user may break Phenox2 by putting it on the serial communication board.) When the main board breaks, no LEDs are lit even if  users turn power switch on. So please take care not to touch the circuit board to other material and make the room always clean.

# About battery
Phenox2 operates 5 minutes on the fly, and 20 minutes on the ground with attached battery (3S, 180mAh). External supply cable should be used instead of battery when users want to use Linux system of Phenox2 for a long time (e.g. installing package from the Internet, or building new software). Also, discarge cables(red and black cable) of the attached battery are removed by us. So when users get a spare battery and want to remove discharge cable. please be careful for not causing short circuit.  

Also, please don't use supply cable when users want to fly Phenox2.

# Changing battery
Before inserting the battery plug to the main board, fix the battery to the protector with rubber band as shown in Fig.1. 
![Fig.1 Fix battery to the protector] (/img/phenox/phenox_battery_1.jpg)
<div align="center">Fig.1 Fix battery to the protector</div>

Then, insert the supply plug to the battery connector of the mainboard as shown in Fig.2. Please be careful not to bend main board.
![Fig.2 Attach battery to the mainboard] (/img/phenox/phenox_battery_2.jpg)
<div align="center">Fig.2 Attach battery to the mainboard </div>

As shown in Fig.3, please attach the protector to the body frame so that you can see the short side of battery from back side of the bode frame.
![Fig.3 Battery direction] (/img/phenox/phenox_battery_5.jpg)
<div align="center">Fig.3 Battery direction </div>

When removing battery, remove rubber band and protector first, and  put your hand as shown in Fig.4. The way shown Fig.5 is not good because bending power to the main board is too strong, which may cause serious breakdown of the mainboad.
![Fig.4 Remove battery(good way)] (/img/phenox/phenox_battery_3.jpg)
<div align="center">Fig.4 Remove battery(good way) </div>

![Fig.5 Remove battery(bad way)] (/img/phenox/phenox_battery_4.jpg)
<div align="center">Fig.5 Remove battery(bad way) </div>


# Start operating Phenox2 with battery
1. Check that voltage of the battery is between 11.6V ~ 12.5V. Also, check the power switch is off state.  
2. Attach battery to the main board as described above. Also, check that propellers can rotate smoothly without interfering other objects.  
3. Insert the microSD card.  
4. Check that two camera boards are attached to the main board.  
5. Check that 4 corners of main board are fixed to silicon ring correctly. 
6. Plese boot Linux as described in [Communication](com.md).  


# Start operating Phenox2 with external supply cable
1. Check the power switch is off state.  
2. Attach the external supply cable to the mainboard as described above. attach a plug of DC12V supply source(it is not included in Phenox2 kit) to the external supply cable.  
3. Insert the microSD card.  
4. Check that two camera boards are attached to the main board.  
5. Plese boot Linux as described in [Communication](com.md).  

