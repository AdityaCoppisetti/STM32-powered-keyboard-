# STM32-powered-keyboard

for my past keyboard build i used an external devboard , the raspberry pico, to operate the board 
as you can see in my project keylouder - https://github.com/AdityaCoppisetti/keylouder .

<img width="180" height="440" alt="image" src="https://github.com/user-attachments/assets/e9e3389f-254e-4b3e-8a47-758d3dca4ec2" />


BUT the challenge with that was that it required alot of external space for the devboard to be in and therefore i had extra
space on the pcb , which gave me the idea of adding modules. however for this pcb i want a proper 60% keyboard with no extra gimmicks. 

for this pcb i will be using the STM32F072CBTx 
The STM32F072 is a series of 32-bit ARM Cortex-M0 microcontrollers manufactured by STMicroelectronics, designed for applications requiring crystal-less USB 2.0 connectivity and high-speed CAN bus integration.

this is a very popular microcontroller and many people often use it to build flight controllers.

for my past builds i was either using the raspberry pico , the arduino nano or oh my god the esp32 ( why the oh my god? BECAUSE IVE BUILT A DEVBOARD AROUND THE ESP32 ABOUT 23 TIMES NOW AND ITS ALWAYS THE SAME)

So i thought using this chip would be really cool

# Here are the features of the chip- 

<img width="667" height="743" alt="image" src="https://github.com/user-attachments/assets/3617ae94-140b-463a-9457-7f2f00675627" />

this is taken from a datasheet , you can look it up. but if you want one , here is the exact link!

https://www.alldatasheet.com/datasheet-pdf/download/1373176/STMICROELECTRONICS/STM32F072CBT6.html


# pinout of the chip - 

<img width="671" height="609" alt="image" src="https://github.com/user-attachments/assets/030d3d06-bfac-40b4-b952-aeb3df5921f6" />

now before we start plotting the schematic , we need to understand what we would have to plot. 

its mainly all the same 
Like reset button , usb and allat , but for this chip we need to have precise esd protection and then voltage regulation , lets see what info we have in the datasheet

# the voltage regulator 

here is what the datasheet says - 

<img width="557" height="161" alt="image" src="https://github.com/user-attachments/assets/7b540d89-1ea7-4e91-9220-e037158ecf81" />

and then the ESD protection.

# ESD protection

<img width="663" height="178" alt="image" src="https://github.com/user-attachments/assets/c1818b66-9b94-4d1c-b01e-788601b860bb" />



#PLOTTING THE SCHEMATIC


