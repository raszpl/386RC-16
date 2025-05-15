# Modular Circuit Technology 386RC-16 ram board
[<img src="img/386RC-16 c.jpg" width='300'>](/img/386RC-16.jpg?raw=true)[<img src="img/386RC-16%20render%20c.png" width='300'>](/img/386RC-16%20render.png?raw=true)

[<img src="img/386RC-16 back c.jpg" width='300'>](/img/386RC-16%20back.jpg?raw=true)[<img src="img/386RC-16%20render%20b%20c.png" width='300'>](/img/386RC-16%20render%20b.png?raw=true)

Reverse Engineered non standard ram expansion board for use in Modular Circuit Technology C386-33.

[<img src="img/C386-33 c.jpg" width='200'>](/img/C386-33.jpg?raw=true)[<img src="img/386RC-16 plugged into C386-33 c.jpg" width='200'>](/img/386RC-16%20plugged%20into%20C386-33.jpg?raw=true)

Diagram ([png](/386RC-16%20diagram.png?raw=true),[pdf](/386RC-16.pdf?raw=true)). Interesting detail about design - it exposes two ways of driving CAS (Column Address Strobe) signals. Designer made it flexible enough to be able to work with different memory controllers/interleave configurations. One set of four CAS pins drives consecutive SIMM sockets in every Bank, the other 4 pin set drives whole banks per CAS line. Brilliant.

Potentially also compatible motherboards:
- [Modular Circuit Technology MCT-C386-33/40](https://theretroweb.com/motherboards/s/auva-computer-tam-33-p2)
- Northgate Computer Systems
  - [NORTHGATE 386](https://theretroweb.com/motherboards/s/northgate-comput-northgate-386)
  - [386/486/486SX (386 BOARD)](https://theretroweb.com/motherboards/s/northgate-comput-386-486-486sx-386-board)
  - [386/486/486SX (486 BOARD)](https://theretroweb.com/motherboards/s/northgate-comput-386-486-486sx-486-board)
- NOVACOR, INC.
  - [OPTIMUM 386WB CACHE](https://theretroweb.com/motherboards/s/novacor,-inc.-optimum-386wb-cache)
  - [SUPER 386](https://theretroweb.com/motherboards/s/novacor,-inc.-super-386)
- [QDI P386](https://theretroweb.com/motherboards/s/qdi-p386)
- [Iwill 80386 WRITE BACK CACHE](https://theretroweb.com/motherboards/s/iwill-80386-write-back-cache)
- Shuttle
  - [HOT-304](https://theretroweb.com/motherboards/s/shuttle-hot-304)
  - [HOT-307](https://theretroweb.com/motherboards/s/shuttle-hot-307)
- [Digicom DIGIS-386WB](https://theretroweb.com/motherboards/s/digicom-digis-386wb)

**Incompatible** platforms using similar slot:
- [Modular Circuit Technology MCT-386-M](https://dosreloaded.de/forum/thread/330-modular-circuit-technology-386dx20-fullsize-at-mainboard)  [<img src="img/not%20compatible/MCT-386-M c.jpg" width='200'>](/img/not%20compatible/MCT-386-M%20c.jpg?raw=true)[<img src="img/not%20compatible/MCT-386-M RAM CARD c.jpg" width='200'>](/img/not%20compatible/MCT-386-M%20RAM%20CARD%20c.jpg?raw=true) Grand daddy of C386-33 from 1987, 386DX 20 and IIT FPU 387 20Mhz. Looks like it might be dual layer PCB! :o 
- [OGIVAR, INC. SYSTEM 386](https://theretroweb.com/motherboards/s/ogivar,-inc.-system-386) unlikely as its a 386XS
- [POSITIVE CORPORATION PC340](https://theretroweb.com/motherboards/s/positive-corpora-pc340) wrong slot position
- [ECS 386A](https://theretroweb.com/motherboards/s/ecs-386a) Same Chips & Technologies CS8230 chipset, same slot, not sure about slot position
- Micronics
  - [386 Baby Non Cache (386/25) (09-00065-xx.)](https://theretroweb.com/motherboards/s/micronics-386-baby-non-cache-386-25-09-0006)
  - [80386 SMT ASIC, 386 ASIC CACHE VER. 4.0 (09-00035-xx/09-00066-xx)](https://theretroweb.com/motherboards/s/micronics-80386-smt-asic,-386-asic-cache-ve)
  - [Baby Gemini 386-33 (09-00086-xx)](https://theretroweb.com/motherboards/s/micronics-baby-gemini-386-33-09-00086-xx)
  - [BABY GEMINI-386 ISA/LB](https://theretroweb.com/motherboards/s/micronics-baby-gemini-386-isa-lb)
  - [80386 ASIC](https://theretroweb.com/motherboards/s/micronics-80386-asic) all use wrong slot

# Resources
Those six pictures uploaded by McBierle was the only source of information. Provided all vias, back tracks and about 25% front ones. Rest is obscured by components and had to be deduced logically using knowledge of vintage memory subsystems.

[<img src="img/386RC-16%20c.jpg" width='200'>](/img/386RC-16.jpg?raw=true)[<img src="img/386RC-16%20back%20c.jpg" width='200'>](/img/386RC-16%20back.jpg?raw=true)

[<img src="img/386RC-16%20front%20left%20c.jpg" width='200'>](/img/386RC-16%20front%20left.jpg?raw=true)[<img src="img/386RC-16%20front%20right%20c.jpg" width='200'>](/img/386RC-16%20front%20right.jpg?raw=true)

[<img src="img/386RC-16%20rear%20left%20c.jpg" width='200'>](/img/386RC-16%20rear%20left.jpg?raw=true)[<img src="img/386RC-16%20plugged%20into%20C386-33%20c.jpg" width='200'>](/img/386RC-16%20plugged%20into%20C386-33.jpg?raw=true)

-----
McBierle authored Vogons [Story about C386-33 and me](https://www.vogons.org/viewtopic.php?t=67359) thread.

# Status

100% reconstructed schematic. 95% ready for manufacturing, remaining tasks:
- Slot position is hard to judge from pictures picture alone due to lens distortion (perspective, pillow). I had to undistort them using [ShiftN](https://www.shiftn.de/ShiftN_functionality.html) and Gimp.
- Dimensions are slightly off, clearances need real measurements.
- Hard to guess which Edge Connector power pins are 5V/Ground on the connector. Only half has tantalums with painted polarization. Better to measure and verify.
- I didnt bother with decoupling capacitors before confirming dimensions.

# Progress report

5/15/2025: Got bored and played with routing. Old board [100% following original track/via layout](https://github.com/raszpl/386RC-16/releases/tag/0.1) had track length 3360cm and 381 vias. New optimized layout track length 3341 cm, 349 vias. 20cm shorter tracks and 30 less vias, nice.

[100% schematic](/386RC-16%20diagram.png?raw=true). 100% electrical PCB. Woke up, looked at the CAS mess and immediatelly knew how to route it, magic of a good night's sleep! 0 ERC, 0 DRC errors. 1 DRC warning for unused Via. No idea if original Designer left it unused or somehow routed the board in different way. Personally I dont see a way to use this Via in any way :)

11/9/2024: [100% schematic](/386RC-16%20diagram.png?raw=true). 100% electrical PCB. Woke up, looked at the CAS mess and immediatelly knew how to route it, magic of a good night's sleep! 0 ERC, 0 DRC errors. 1 DRC warning for unused Via. No idea if original Designer left it unused or somehow routed the board in different way. Personally I dont see a way to use this Via in any way :)

11/8/2024: 95%. SIMM slots and DIP14 chips obscure CAS traces. [Struggling hard with routing CAS lines with all the missing information, still dont undertand purpose of OR gates instead of simple buffers](/img/386RC-16%20diagram%2090%25%20WTF%20CAS.png)

11/7/2024: 85-90% Got RAS mapping correct. [90% back](/img/386RC-16%20diagram%2090%25.png)

11/6/2024: 60-80%. Deduced Address/WE buss pairing, Address/Data buss Edge Slot pinout. Still ~300 ERC, ~200 ERC errors.

11/5/2024: 65%. Figured all 240/244 chips used same connections to corresponding pair of Resistor Pair Packs, Designer copy pasted it 12 times.

11/4/2024: 60%. Further fixed picture distortions wih Gimp Transform functionality (what a pain!). Allowed almost ideal component placement and drawing board outline.

10/31/2024: Very VIP. Preliminarily undistorted source pictures using [ShiftN](https://www.shiftn.de) to help with more precise component placement. [10% there front](/img/386RC-16%20about%2010%25.jpg)[10% back](/img/386RC-16%20about%2010%25b.jpg)

10/30/2024: Project start. Looking at pictures of 386RC-16 uploaded by McBierle on vogons forum and assesing feasibility. Rougly placing components more or less by eye and tracing few lines. [1% there](/img/386RC-16%201%25.jpg)

-----------------
# Work for hire
Interested in having a piece of hardware reverse engineered/cloned? Drop me an [email](https://github.com/raszpl).
