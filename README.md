# DIY-21700-Battery-System
This is a do-it-yourself battery system using 21700-form-factor cells, intended for use on UAVs or UGVs. The parametric nature of the system allows designing and building a lithium ion battery system specific to your vehicle's requirements. The value add is threefold:
1) you can use your choice of cells
2) you enjoy a 50% discount by building it yourself
3) the battery has a press-to-release latching mechanism, which gives a common interface for battery swapping (either manually or by robot arm)

## Use of 21700 Cells
Cylindrical cells having 21[mm] height and 70[mm] length (i.e. 21700 cells) are used since they are cheap, easily obtained, and have high gravimetric energy density. In comparison to other cells types, 18650 cells tend to have lower gravimetric energy density, while 4680 cells, prismatic cells, and pouch cells aren't widely available to the general public (as of late 2026).

## The Battery System
The battery system consists of the following components:
1) the battery
2) the vehicle adapter
3) the charger

Each component is sized according to the chosen battery configuration. Possible battery configurations are:
* Six in series:
    - Three in parallel (6s3p)
    - Four in parallel (6s4p)
    - Five in parallel (6s5p)
    - Six in parallel (6s6p)
* Eight in series:
    - Three in parallel (8s3p)
    - Four in parallel (8s4p)
    - Five in parallel (8s5p)
    - Six in parallel (8s6p)
* Ten in series:
    - Three in parallel (10s3p)
    - Four in parallel (10s4p)
    - Five in parallel (10s5p)
    - Six in parallel (10s6p)
* Twelve in series:
    - Three in parallel (12s3p)
    - Four in parallel (12s4p)
    - Five in parallel (12s5p)
    - Six in parallel (12s6p)

## Steps for Selecting a Battery Configuration
1) Decide the max payload mass, and the max vehicle range or endurance
2) Using a battery mass fraction of 66%, estimate the total vehicle mass
3) Select the motors to be used in the vehicle, then use the motor's max voltage rating as the battery's max voltage, and then calculate the expected max discharge rate (in Amps) using the motor's thrust table (should be provided with the motor, and should list the thrust, efficiency, and current draw at each throttle percentage corresponding to each motor-prop pair)
4) Determine the battery's number of cells in series ((nominal voltage required)/(cell voltage))
5) Determine the number of cells in parallel (max battery discharge rate)/(max cell discharge rate), and select the 21700 cell having the highest charge capacity for the intended discharge rate. This is iterative. **NEEDS CLARIFICATION. NEEDS TO TAKE INTO ACCOUNT THE RANGE/ENDURANCE REQUIREMENTS.**

## Battery Naming Convention
	21700_MsNp
	where
	M = number of cells in series
	N = number of cells in parallel

	For example...
	21700_6s4p indicates a battery using cylindrical cells having diameter of 21[mm] and length of 70[mm], with 6 cells in series and 4 cells in parallel
	The total number of cells used in this battery is M*N = 6*4 = 24

