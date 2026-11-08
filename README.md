# PowerGen
A portable(-ish) power generator. That is made using a NEMA 23, a gear ratio and power is made by turning a hand crank.

# What is it?
Power Gen is my idea of a off grid power bank. It is a prototype and partly designed. It has sufficient components to work but not extra because the budget was right.

Choosing the Gear Configuration

For the drivetrain, I decided to design a set of straight spur gears to achieve the necessary speed step-up ratio. Since these are being exported for a high-resolution resin print from JLC3DP, I am keeping the gear tolerances tight in CAD, though I will need to account for a tiny bit of material shrinkage so the teeth mesh nicely without binding.

Maximizing Electrical Efficiency

On the electronics side of the design, the plan is to route the motor's AC output into a rectifier bridge made of Schottky diodes. I chose these in my schematic because of their low forward voltage drop, which ensures that even slower, casual turns of the hand crank won't completely lose their voltage to circuit inefficiencies.

Organizing the Power Bank

The base of the CAD enclosure is designed around a 3S2P 18650 battery bank layout, which gives me a solid footprint to work with. To bridge the gap between my hand-cranking and the battery cells, I'm leaving ample room in the housing to mount a buck-boost regulator and a protective BMS to keep the incoming power clean and safe.

# CAD
I did lots of CAD 

<img width="796" height="623" alt="Screenshot 2026-11-08 204945" src="https://github.com/user-attachments/assets/73361538-b578-41d0-afad-8d07bf49bdfa" />
<img width="685" height="479" alt="Screenshot 2026-11-08 205002" src="https://github.com/user-attachments/assets/da3a070d-e000-485e-a85c-21a97a16de4c" />
<img width="265" height="216" alt="Screenshot 2026-11-08 205130" src="https://github.com/user-attachments/assets/387c8535-2009-4177-ab3e-65fb0f3d6f10" />
<img width="887" height="570" alt="Screenshot 2026-11-08 205052" src="https://github.com/user-attachments/assets/987d3012-e63c-491a-a339-4b9298865543" />
<img width="667" height="467" alt="image" src="https://github.com/user-attachments/assets/e82847f4-a95c-4818-b924-c1937370ac4a" />
