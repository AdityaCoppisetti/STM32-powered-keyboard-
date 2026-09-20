## STM32-powered-keyboard

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

Features
• Core: Arm® 32-bit Cortex®-M0 CPU, frequency
up to 48 MHz
• Memories
– 64 to 128 Kbytes of Flash memory
– 16 Kbytes of SRAM with HW parity
• CRC calculation unit
• Reset and power management
– Digital and I/O supply: VDD = 2.0 V to 3.6 V
– Analog supply: VDDA = VDD to 3.6 V
– Selected I/Os: VDDIO2 = 1.65 V to 3.6 V
– Power-on/Power down reset (POR/PDR)
– Programmable voltage detector (PVD)
– Low power modes: Sleep, Stop, Standby
–VBAT supply for RTC and backup registers
• Clock management
– 4 to 32 MHz crystal oscillator
– 32 kHz oscillator for RTC with calibration
– Internal 8 MHz RC with x6 PLL option
– Internal 40 kHz RC oscillator
– Internal 48 MHz oscillator with automatic
trimming based on ext. synchronization
• Up to 87 fast I/Os
– All mappable on external interrupt vectors
– Up to 68 I/Os with 5V tolerant capability
and 19 with independent supply VDDIO2
• 7-channel DMA controller
• One 12-bit, 1.0 µs ADC (up to 16 channels)
– Conversion range: 0 to 3.6 V
– Separate analog supply: 2.4 V to 3.6 V
• One 12-bit D/A converter (with 2 channels)
• 2 fast low-power analog comparators with
programmable input and output
• Up to 24 capacitive sensing channels for
touchkey, linear and rotary touch sensors
• Calendar RTC with alarm and periodic wakeup
from Stop/Standby
• 12 timers
– One 16-bit advanced-control timer for
six-channel PWM output
– One 32-bit and seven 16-bit timers, with up
to four IC/OC, OCN, usable for IR control
decoding or DAC control
– Independent and system watchdog timers
– SysTick timer
• Communication interfaces
– 2 I2C interfaces supporting Fast Mode Plus
(1 Mbit/s) with 20 mA current sink, one
supporting SMBus/PMBus and wakeup
– 4 USARTs supporting master synchronous
SPI and modem control, two with ISO7816
interface, LIN, IrDA, auto baud rate
detection and wakeup feature
– 2 SPIs (18 Mbit/s) with 4 to 16
programmable bit frames, and with I2S
interface multiplexed
– CAN interface
– USB 2.0 full-speed interface, able to run
from internal 48 MHz oscillator and with
BCD and LPM support
• HDMI CEC wakeup on header reception
• Serial wire debug (SWD)
• 96-bit unique ID
• All packages ECOPACK®2
