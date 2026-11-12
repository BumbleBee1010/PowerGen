# PowerGen
A portable(-ish) power generator. That is made using a NEMA 23, a gear ratio and power is made by turning a hand crank. PowerGen is my idea of a off grid power bank. It is a prototype and partly designed and is a first iteration on a tight budget.

## How does it work?
For the drivetrain, I decided to design a set of straight spur gears to achieve the necessary speed step-up ratio. So the hand crank generates enough force to turn the motor and generate voltage, about 20v to 35v I think it will achieve. This generated power will then be fed into a 3s2p 18650 powerbank and then that will output into 2 dual usb c chargers. 

## PCB changes and results
### Schematic
Originally, I was planning to add a usb c PD port and multiple usb a ports but then I realised it would push me way over budget so I decided to cut it and just use usb c, which is more common nowdays. It wasn't a big difference to change compared to the old schematic, however, I needed to remove/ repurpose some of the screw terminals.

<img width="635" height="420" alt="image" src="https://github.com/user-attachments/assets/2d7dd09d-7a91-4be6-9085-c7fcaafd0b2f" />
New schematic

<img width="635" height="420" alt="Screenshot 2026-11-08 100136" src="https://github.com/user-attachments/assets/6eb076c5-7b33-4591-b375-f40b550d4731" />
Old schematic


### Layout
I did two versions of the PCB, one a 75 by 75 mm board and another smaller one. The main reason I changed the board was because it was too large but I now also realised that I had the wrong completely oversized capacitor in the first version which could have messed thing up. On the PCB, the plan is to route the motor's AC output into a rectifier bridge made of Schottky diodes, this should cause less of a voltage drop and output smoother voltage needed to go into the buck convertor. You can see on the images of the PCB that there are quite a few screw terminals dotted around the edge (and labelled) this is how all the components will connect. You can say the PCB is a hub for all the components. I will use 18 AWG wire to wire all the components together.

<img width="323" height="296" alt="Screenshot 2026-11-12 073739" src="https://github.com/user-attachments/assets/595365eb-296a-4d28-927f-001255d30fb8" />
<img width="380" height="379" alt="Screenshot 2026-11-12 073757" src="https://github.com/user-attachments/assets/88260640-ee62-4e0a-84e1-0b500b138df8" />
New designs

<img width="380" height="379" alt="image" src="https://github.com/user-attachments/assets/2fbde91d-10c4-4758-b593-f40780192cb6" />
Old design

# CAD
I did lots of CAD

<img width="796" height="623" alt="Screenshot 2026-11-08 204945" src="https://github.com/user-attachments/assets/73361538-b578-41d0-afad-8d07bf49bdfa" />
<img width="685" height="479" alt="Screenshot 2026-11-08 205002" src="https://github.com/user-attachments/assets/da3a070d-e000-485e-a85c-21a97a16de4c" />
<img width="265" height="216" alt="Screenshot 2026-11-08 205130" src="https://github.com/user-attachments/assets/387c8535-2009-4177-ab3e-65fb0f3d6f10" />
<img width="887" height="570" alt="Screenshot 2026-11-08 205052" src="https://github.com/user-attachments/assets/987d3012-e63c-491a-a339-4b9298865543" />
<img width="667" height="467" alt="image" src="https://github.com/user-attachments/assets/e82847f4-a95c-4818-b924-c1937370ac4a" />
