# RP2350A IMU Dev Board

A custom dev board built around the RP2350A microcontroller with an 
onboard MPU-6050 IMU for motion sensing, housed in a custom 3D printed case.

PCB Render:<img width="524" height="593" alt="Screenshot 2026-05-29 at 9 38 06 PM" src="https://github.com/user-attachments/assets/9d4385f2-188f-46df-96a4-330f4886fe5d" />


## How it works

The board uses a USB-C connector and an AMS1117-33 LDO to regulate 
5V down to 3.3V. The RP2350A runs with a 12MHz crystal oscillator and 
W25Q128 flash memory over QSPI. The MPU-6050 IMU connects over I2C on 
GPIO4 and GPIO5 for motion sensing. GPIO headers expose the remaining 
pins for external use.

KiCanvas Link: https://kicanvas.org/?repo=https%3A%2F%2Fgithub.com%2FNxyz-natan%2Fweek-7-and-8-resolution-hardware%2Ftree%2Fmain%2Fsrc%2Fkicad

Case Design Link: https://app.shapr3d.com/p/ce0b803e-1716-4454-bb49-c60d17f44aa6



## Schematic

![Schematic] <img width="886" height="627" alt="Screenshot 2026-05-29 at 9 38 57 PM" src="https://github.com/user-attachments/assets/e98a122f-7d2d-4633-b5ac-76734cb973d2" />


## PCB

![PCB] <img width="510" height="646" alt="Screenshot 2026-05-29 at 9 39 11 PM" src="https://github.com/user-attachments/assets/ecbf1a69-9447-4bc6-ad20-a56e4498797c" />


## Case

![Case <img width="791" height="608" alt="Screenshot 2026-05-29 at 9 39 25 PM" src="https://github.com/user-attachments/assets/1dde3525-90ba-40ba-a5d7-2ffd42d81f71" />


---

## Bill of Materials

| Ref | Value | Qty | LCSC # |
|-----|-------|-----|--------|
| U1 | RP2350A | 1 | C42411118 |
| U2 | W25Q128JVSIQ | 1 | C97521 |
| U3 | AMS1117-3.3 | 1 | C6186 |
| U4 | MPU-6050 | 1 | C24112 |
| R1, R2 | 5.1k 0603 | 2 | C2907044 |
| R3 | 1k 0603 | 1 | C22548 |
| R4, R5 | 27Ω 0603 | 2 | C137753 |
| R6, R7 | 10k 0603 | 2 | TBD |
| R8, R9 | 4.7k 0603 | 2 | C99782 |
| C1-C4 | 1uF 0603 | 4 | C15849 |
| C5-C11, C14-C18 | 100nF 0603 | 13 | C14663 |
| C12, C13 | 15pF 0603 | 2 | C1644 |
| Y1 | 12MHz Crystal SMD3225 | 1 | C9002 |
| J1 | USB-C TYPE-C-31-M-12 | 1 | C165948 |
| J2 | 1x04 Pin Header 2.54mm | 1 | C52016392 |
| J4 | 1x20 Pin Header 2.54mm | 1 | C50981 |
| J5 | 1x13 Pin Header 2.54mm | 1 | C42372505 |
| SW1, SW2 | SW Push 6x6mm | 2 | C318884 |
