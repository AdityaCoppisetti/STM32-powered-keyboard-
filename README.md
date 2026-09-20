# STM32-powered-keyboard

for my past keyboard build i used an external devboard , the raspberry pico, to operate the board 
as you can see in my project keylouder - https://github.com/AdityaCoppisetti/keylouder .

<img width="1258" height="447" alt="image" src="https://github.com/user-attachments/assets/af4a0bda-25b3-42bd-bd33-c61d6b25a206" />



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



# PLOTTING THE SCHEMATIC

We start off with the MCU

## the STM32 pinout is like this 

<img width="593" height="897" alt="image" src="https://github.com/user-attachments/assets/63b5271e-db10-4712-9ef3-57e832617c94" />

i really like labeling my schematic neatly so i use lines to point and reason why im using what and what it does 

then to label its pins ive used global net labels 

and then we need the - 

# DECOUPLING CAPACITORS

<img width="734" height="330" alt="image" src="https://github.com/user-attachments/assets/5591ebe5-ae06-4f23-9f66-c0fd93881ca6" />

decoupling capacitors are used to make the power flow reliable and stable 

and then we have the 

# boot/ reset button


<img width="386" height="388" alt="image" src="https://github.com/user-attachments/assets/dc9e720f-68f1-40de-ab95-42d7345c58f0" />

this is there so we can load the firmware onto the chip

it is connected to the BOOT pin on the chip via a global net label 


and then here is both the **ESD protection** and the **Voltage step down** 

<img width="905" height="376" alt="image" src="https://github.com/user-attachments/assets/618d999d-bb6a-405a-8bbd-1f855b76002d" />


and then i have the usb connection , which is lowkey just normal besides the fact ive added a 500mA fuse 

<img width="725" height="876" alt="image" src="https://github.com/user-attachments/assets/c80c110b-b8d5-4a8f-9aa6-346b271037fe" />

and once again ive labeled it nicely 

before we move onto building the pcb , lets define the footprints


# FOOTPRINTS 

<img width="717" height="424" alt="image" src="https://github.com/user-attachments/assets/bc6e3535-d4ea-49f7-847f-ebe1b4902058" />

oops it seems i forgot to asign a footprint to a resister

just asign it the same as others

# NOW LETS BUILD THE PCB 

we have to open the pcb editor and import our parts by updating the pcb 

<img width="737" height="719" alt="image" src="https://github.com/user-attachments/assets/7044cddb-c72b-4694-8093-478302eca523" />


also i accidentally connected the boot button to +3V3 when its supposed to be +3.3V

<img width="556" height="537" alt="image" src="https://github.com/user-attachments/assets/e69c0cff-44ba-4696-b7bb-c17256b0af8d" />
