# -PLC- SHORTING BASED ON WEIGHT

**Shorting based on weight** is a PLC based industrial application for 
shorting boxes based on their weight (Small, Medium, Large).
Tia portal V15 has been used for the programing.
Factory i/o has been used for the 3D simulation. 
S7-PLCSIM has been used instead of a real PLC.


## Main Idea
You can choose between three recipes for shorting:
- **recipe 0** : Small(Left), Large(Forward), Medium(Right)
- **recipe 1** : Medium(Left), Small(Forward), Large(Right)
- **recipe 2** : Large(Left), Medium(Forward), Small(Right)

The boxes are on the `belt conveyor` where a `Conveyor Scale` weights them and depend on the recipe a `double-sided pop-up wheel sorter` divert them to three different directions.
In the end of The conveyors the boxes are counted with the help of `Diffuse photoelectric sensors`.
Next to The Station is an `Electric Switchboard` with three `Push Buttons` (start, stop and reset counters) 
, a `two position red trigger action push button` used for emergency stop, three screens to display the counter values and one screen to display the weight of every box.
You can use the `HMI screen` to choose the recipe and to check which recipe is on.





## Devices

- **PLC**:  `S7-1200`,

    **CPU**: `1211C DC/DC/DC`,

    **Description** : Work memory 50 KB; 24VDC power supply with DI6 x 24VDC SINK/ SOURCE, DQ4 x 24VDC and AI2 on
board;3 high-speed counters (expandable with digital signal board) and 4 pulse outputs on board; signal board expands on-board I/O; up to 3 communication modules for serial communication; 0.04 ms/1000 instructions; PROFINET interface for programming, HMI and PLC to PLC communication


- **HMI**: `KTP700 Basic PN`

## IMAGES

**FACTORY IO IMAGE**
![S.B.W.factory.jpg](/img/S.B.W.factory.jpg)

**HMI IMAGE**
![S.B.W.HMIjpg.jpg](/img/S.B.W.HMIjpg.jpg)


## Files

- **ShortingByWeightCode.pdf** : it's the plc code
- **ShortingByWeightHmi.pdf** : it's the HMI settings
- **ShortingByWeightVideo.mkv** : it's a demonstration of how it works
- **shortingByWeight.factoryio** : it's the factory io file 
- **shorting by weight** : it's the folder for the tia portal
