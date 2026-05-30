
# RP2350A IMU Dev Board

[Preface] I'm building a custom dev board around the RP2350A because 
I wanted to design my own PCB from scratch with an onboard IMU for 
motion sensing.

## May 27 - Schematic Design

Today I worked on the full schematic in KiCad. I started with the 
power section using a USB-C connector and an AMS1117-33 LDO to bring 
5V down to 3.3V. Then I wired up the RP2350A with:

- Decoupling caps on all power pins
- A 12MHz crystal oscillator
- W25Q128 flash memory over QSPI
- USB data lines with 27Ω series resistors
- A reset button on the RUN pin
- A boot button on QSPI_SS
- An MPU-6050 IMU over I2C on GPIO4 and GPIO5
- Two GPIO headers to expose pins

I ran into an issue with the USB-C wiring where I put the 51k CC 
resistors on the wrong pins. I researched how USB-C CC pins work and 
found they handle power negotiation with the host, so I moved them to 
the correct pins and it worked fine after that.

I also had trouble routing the PCB since everything was very tight and 
I couldn't manage to wire 4 GPIO pins. I went back to the schematic 
and reassigned those pins to VBUS, GND, and 3V3 instead which made 
routing much cleaner.

### Time Spent: 4 Hours

## May 27 - Case Design

Today I designed a case for the dev board in Shapr3D.

I started by exporting the PCB as a STEP file from KiCad and importing 
it into Shapr3D to use as a reference for the case dimensions. I 
designed the case in two parts — a bottom tray and a top lid — with 
1.5mm screw holes in each corner so the two pieces can be fastened 
together with M2 screws.

I added cutouts for the USB-C port and GPIO headers so they remain 
accessible when the case is closed. I also added "Dev Board" text on 
the bottom of the case using the emboss tool to give it a personal touch.

The main challenge was getting the screw holes to fit without cracking 
the walls since the case walls were thin. I reduced the hole size to 
1.5mm and placed them at the corners where the walls were thickest.

### Time Spent: 2 Hours
