# week-7-hardware-resolution
RP2350A IMU Dev Board
I'm building a custom dev board around the RP2350A because I wanted to design my own PCB from scratch and have something unique with an onboard IMU for motion sensing
May 27 - Schematic Design
Today I worked on the full schematic for my RP2350A dev board in KiCad I started with the power section using a USB-C connector and an AMS1117-33 LDO to bring 5V down to 33V Then I wired up the RP2350A with decoupling caps on all the power pins, a 12MHz crystal oscillator, W25Q128 flash memory over QSPI, USB data lines with 27Ω series resistors, a reset button on the RUN pin, a boot button on QSPI_SS, and an MPU-6050 IMU over I2C on GPIO4 and GPIO5 I also added two GPIO headers to expose the pins here is the schematic 
<img width="876" height="629" alt="Screenshot 2026-05-27 at 9 07 04 PM" src="https://github.com/user-attachments/assets/d65614f2-0e15-4436-b47c-ef81feaa7ee4" />

and then i went a put all my components and wired them up here is my pcb <img width="512" height="686" alt="Screenshot 2026-05-27 at 9 06 48 PM" src="https://github.com/user-attachments/assets/0a4e2c7b-1691-406f-9ccd-524e247ddf58" />

and pcb render 
<img width="386" height="378" alt="Screenshot 2026-05-27 at 9 06 43 PM" src="https://github.com/user-attachments/assets/683a4efb-661f-47fa-9b29-c2a1f2b34876" />



I ran into issues with the USB-C wiring where I put the 51k CC resistors on the wrong pins at first I looked into how USB-C CC pins work and found they handle power negotiation with the host so I moved them to the correct pins and it was fine after that and also had issue with actually wiring the pcb since it was all tight and couldnt managed to wire 4 gpio so i went to the schematics and changed them pins to vbus,gnd, and 3v3
Time Spent: 4 Hours
