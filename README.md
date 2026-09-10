# DIY-21700-Battery-System
## Overview
This is a do-it-yourself battery system intended for use with Unmanned Aerial Vehicles or Unmanned Ground Vehicles. It consists of 
1) a battery using lithium ion 21700-form-factor cells\
   [PUT IMAGE HERE]
   
2) a vehicle adapter with place-to-lock/press-to-unlock latching mechanism\
   [PUT IMAGE HERE]
   
3) an off-vehicle charging station\
   [PUT IMAGE HERE]

The parametric nature of this system allows designing and building a battery system specific to your vehicle's requirements. As such, the value add of such a system is threefold:
1) you can use cells of your choice (i.e., can optimize for either power output or energy capacity)
2) you can enjoy a 50% discount by building it yourself
3) the battery's latching mechanism presents a common interface for battery swapping (either manually or by robot arm), which vastly increases system uptime when compared to on-board charging

Additionally, safety is paramount. A temperature sensor circuit consisting of a microcontroller and thermistors is used to monitor the temperature at each cell station on the battery during flight, with options of alerting the pilot or autolanding the vehicle if a measured temperature exceeds some threshold temperature (e.g., 80% of thermal runaway temperature). The circuit itself is integrated into the battery power PCB, conveniently tucked away within the battery itself. The temperature sensor microcontroller communicates with the flight controller via I2C ports located next to the power connecter on the bottom surface of the battery. **Currently, the firmware for temperature sensing functionality is implemented for vehicles using Ardupilot control software, however, functionality with PX4 is in-progress.**

Cylindrical cells having 21[mm] height and 70[mm] length (i.e. 21700 cells) are used in the battery since they are cheap, easily obtained, and have high gravimetric energy density. In comparison to other cells types, 18650 cells tend to have lower gravimetric energy density, while 4680 cells, prismatic cells, and pouch cells aren't widely available to the general public (as of late 2026).

Building this system consists of many steps (see 'Pre-build Steps' section and 'Build Steps' section), and requires specific tools (see 'Required Tools' section). As a consequence, many people may find that doing this on their own is too advanced for them. The way I can address this is by selling a build kit: in essence, all you would need to do upon receiving the kit is
1) spot weld the terminals of your favorite cells (purchased separately) to the pre-wired bus bars included in the kit
2) fasten the fully-prepared 3D printed parts and pre-populated PCBs together with screws
3) Test the battery by performing a few charge/discharge cycles your battery charger (battery charger not in the kit)
In this way, all you would need to complete the build is a suitable spot welder, hex wrenches, and a suitable battery charger.
The web store for buying these kits is under development as of 2026/09/08
The link to purchase kits is here [PUT LINK TO WEB STORE]

Whether building from raw materials or building from the kit, pictures and descriptions are provided at each step to aid in the build process.

## Components
The battery system consists of the following components:
1) the battery
2) the vehicle adapter
3) the charger

Each component is sized according to the chosen battery configuration. Possible battery configurations are:
* Six in series:
    - Three in parallel (21700_6s3p)
    - Four in parallel (21700_6s4p)
    - Five in parallel (21700_6s5p)
    - Six in parallel (21700_6s6p)
* Eight in series:
    - Three in parallel (21700_8s3p)
    - Four in parallel (21700_8s4p)
    - Five in parallel (21700_8s5p)
    - Six in parallel (21700_8s6p)
* Ten in series:
    - Three in parallel (21700_10s3p)
    - Four in parallel (21700_10s4p)
    - Five in parallel (21700_10s5p)
    - Six in parallel (21700_10s6p)
* Twelve in series:
    - Three in parallel (21700_12s3p)
    - Four in parallel (21700_12s4p)
    - Five in parallel (21700_12s5p)
    - Six in parallel (21700_12s6p)

## Steps for Selecting a Battery Configuration
In general,\
**The number of cells in series determines the battery voltage:**\
$battery\ max\ voltage = (cell\ max\ voltage) * (number\ of\ cells\ in\ series)$\
where\
$cell\ max\ voltage$ = 4.1 V (for LiIon cells)

**The number of cells in parallel determines the battery charge capacity:**\
$battery\ charge\ capacity = (cell\ expected\ charge\ capacity) * (number\ of\ cells\ in\ parallel)$\
where\
$cell\ expected\ charge\ capacity$ = a function of expected average current draw in cruise (fixed wing) or hover (VTOL)

Specifically, to find the cell's expected charge capacity, check its datasheet for the plot of Voltage vs Charge Capacity, which contains curves of various discharge rates, and then match the expected average current draw to the corresponding discharge rate curve. Finally, find the capacity corresponding to the "empty" voltage of 2.8 V.

For a UAV, the appropriate battery configuration can be determined as follows:
1) Decide the max payload mass, and the max vehicle range or endurance
2) Using a battery mass fraction of 66%, estimate the total vehicle mass
3) Select the motors to be used in the vehicle, then use the motor's max voltage rating as the battery's max voltage, and then calculate the expected max discharge rate (in Amps) using the motor's thrust table (should be provided with the motor, and should list the thrust, efficiency, and current draw at each throttle percentage corresponding to each motor-prop pair)
4) Determine the battery's number of cells in series ((nominal voltage required)/(cell voltage))
5) Determine the number of cells in parallel (max battery discharge rate)/(max cell discharge rate), and select the 21700 cell having the highest charge capacity for the intended discharge rate. This is iterative. **NEEDS CLARIFICATION. NEEDS TO TAKE INTO ACCOUNT THE RANGE/ENDURANCE REQUIREMENTS.**

## Required Tools

## Bill of Materials and Total Cost

## Build Steps
This section describes the build steps for 
1. the battery
2. the vehicle adapter
3. the charging station

### Battery Build Steps
[COMPLETE THIS]

### Vehicle Adapter Build Steps
[COMPLETE THIS]

### Charging Station Build Steps
[COMPLETE THIS]

## FUTURE TO DO
* extend temperature sensor functionality to PX4 control software (currently only works with Ardupilot)
* replace battery latch mechanism push button with internal clamp-to-unlatch mechanism hidden by spring-actuated trap doors: this will enable the battery to fit into a "fuselage cutout" of a fixed-wing UAV without imposing a drag penalty
* make an automated battery swapping system composed of a robot arm, gripper, and some way to precisely orient the gripper to actuate the latching mechanism on the battery
* Complete the battery low voltage alarm (flashing orange LED lights and loud buzzer) and add the details to this project

## IMMEDIATE TO DO
* Take pictures of build steps
* Write out build steps and include pictures here
* Add PCB design files (KiCad project files)
* Add PCB fabrication files (gerber)
* Complete the temperature sensor circuit: use ATtiny3227 microcontroller instead of ATmega328P
* Refactor the steps for selecting the battery configuration of a UAV
* Create steps for selecting the battery configuration of a UGV
