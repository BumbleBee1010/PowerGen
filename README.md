# PowerGen
A portable(-ish) power generator. That is made using a NEMA 23, a gear ratio and power is made by turning a hand crank. PowerGen is my idea of a off grid power bank. It is a prototype and partly designed and is a first iteration on a tight budget.

# How does it work?
For the drivetrain, I decided to design a set of straight spur gears to achieve the necessary speed step-up ratio. So the hand crank generates enough force to turn the motor and generate voltage, about 20v to 35v I think it will achieve. This generated power will then be fed into a 3s2p 18650 powerbank and then that will output into 2 dual usb c chargers. 

# PCB changes and results
## Schematic
Originally, I was planning to add a usb c PD port and multiple usb a ports but then I realised it would push me way over budget so I decided to cut it and just use usb c, which is more common nowdays. It wasn't a big difference to change compared to the old schematic, however, I needed to remove/ repurpose some of the screw terminals.

<img width="635" height="420" alt="image" src="https://github.com/user-attachments/assets/2d7dd09d-7a91-4be6-9085-c7fcaafd0b2f" />
New schematic

<img width="635" height="420" alt="Screenshot 2026-11-08 100136" src="https://github.com/user-attachments/assets/6eb076c5-7b33-4591-b375-f40b550d4731" />
Old schematic


## Layout
I did two versions of the PCB, one a 75 by 75 mm board and another smaller one. The main reason I changed the board was because it was too large but I now also realised that I had the wrong completely oversized capacitor in the first version which could have messed thing up. On the PCB, the plan is to route the motor's AC output into a rectifier bridge made of Schottky diodes, this should cause less of a voltage drop and output smoother voltage needed to go into the buck convertor. You can see on the images of the PCB that there are quite a few screw terminals dotted around the edge (and labelled) this is how all the components will connect. You can say the PCB is a hub for all the components. I will use 18 AWG wire to wire all the components together.

<img width="475" height="400" alt="Screenshot 2026-11-12 073739" src="https://github.com/user-attachments/assets/595365eb-296a-4d28-927f-001255d30fb8" />
<img width="425" height="400" alt="Screenshot 2026-11-12 073757" src="https://github.com/user-attachments/assets/88260640-ee62-4e0a-84e1-0b500b138df8" />
New designs


<img width="400" height="400" alt="Screenshot 2026-11-08 095927" src="https://github.com/user-attachments/assets/7ceb2f9c-bb2e-499d-bb80-41cdc8fe2943" />
Old design

# CAD
I did lots of CAD, I derived the Nema 23, which I got from GrabCAD, and edited it to have a d shaft. Basically did my entire design revolving around that. I started by creating a rough mount shape for the bits to all connect, then I did the gear ratio using GF Gear generator, an addon I installed into Fusion. Then I designed the Handle to attach to the gear, it attaches via some alignment holes and 4 M3 screws which should hopefully be secure enough. The parts are all allowed to spin smoothly because I am going to use bearings and push fit them.

<img width="500" height="350" alt="Screenshot 2026-11-08 204945" src="https://github.com/user-attachments/assets/73361538-b578-41d0-afad-8d07bf49bdfa" />
<img width="500" height="350" alt="Screenshot 2026-11-08 205002" src="https://github.com/user-attachments/assets/da3a070d-e000-485e-a85c-21a97a16de4c" />
<img width="500" height="350" alt="Screenshot 2026-11-08 205130" src="https://github.com/user-attachments/assets/387c8535-2009-4177-ab3e-65fb0f3d6f10" />
<img width="500" height="350" alt="Screenshot 2026-11-08 205052" src="https://github.com/user-attachments/assets/987d3012-e63c-491a-a339-4b9298865543" />
<img width="500" height="250" alt="image" src="https://github.com/user-attachments/assets/e82847f4-a95c-4818-b924-c1937370ac4a" />

# BOM
I did all the prices and it is slightly over the $100 budget, however, coupons and discounts will probably lower this price to be within budget. All the AliExpress stuff is free shipping, only the batteries, stepper and JLC stuff require shipping costs, which is about a quarter if the cost, mainly because of weight and bulk of some of the items and that the stepper and batteries are sourced from Europe/ the UK, which cost slightly more but shipping is infinitely less. 


| Item | Qty | Supplier | Cost/item | Total Cost |
| :--- | :--- | :--- | :--- | :--- |
| Nema 23 stepper 76mm | 1 | StepperOnline | $20.66 | $20.66 |
| 18650s (3500mAh, 10.2A) | 1 | NKON | $15.60 | $15.60 |
| KF301 Screw terminal | 1 | AliExpress | $2.05 | $2.05 |
| SR560 Schottky Diode | 1 | AliExpress | $2.20 | $2.20 |
| 4700µF 63V & 100nf Capacitors | 1 | AliExpress | $2.75 | $2.75 |
| 15A Fuse and Holder | 1 | AliExpress | $1.34 | $1.34 |
| XL4016 buck convertor | 1 | AliExpress | $4.00 | $4.00 |
| USB C dual charger outputs | 2 | AliExpress | $1.08 | $2.16 |
| Switches (2 pin) | 1 | AliExpress | $1.35 | $1.35 |
| 3S 40a balanced BMS | 1 | AliExpress | $1.80 | $1.80 |
| Bearings | 1 | AliExpress | $1.35 | $1.35 |
| Wire & nickel strips | 1 | AliExpress | $6.50 | $6.50 |
| JLC stuff | 1 | JLC PCB & 3DP | $15.50 | $15.50 |
| Exxchange rate fluctuation | 1 | Xe | $0.20 | $0.20 |
| Estimated total shipping | 1 | | | $25.50 |
| Estimated total | | | | *$102.96* |

If you wish to find parts link, please look at the BOM.csv in files
