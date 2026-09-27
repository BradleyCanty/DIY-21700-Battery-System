# Battery Build Instructions

## Outline
1. 3D Print the Parts
2. Assemble the End Plates
3. Calculate Battery Busbar Size & Quantity
4. Prepare the Busbars
5. Place Cells in Frames & Spot Weld Busbars to Cells
6. Wire-up the Power & Balance Connectors
7. Attach Bottom, Top, & End Plates
8. Battery Cell Voltage Check & First Charge-up

---

## 1) 3D Print the Parts

| Part | Quantity | Filament | Print Settings |
| :--- | :--- | :--- | :--- |
| [Frame](LINK HERE) | 2 | black ASA | 100% infill |
| [Top plate](LINK HERE)  | 1 | black ASA | 15% infill |
| [Bottom plate](LINK HERE)  | 1 | black ASA | 15% infill, requires supports |
| [End plate](LINK HERE)  | 2 | black ASA | 15% infill |
| [End plate cover](LINK HERE)  | 2 | black ASA | 15% infill, requires supports |
| [End plate clamp](LINK HERE)  | 4 | white ASA | 100% infill, requires supports |
| [End plate button](LINK HERE)  | 2 | white ASA | 15% infill |

---

## 2) Assemble the End Plate

2.1) Using metal shears, cut the arms of the two torsion springs to length of 15mm, as measured from the center of the coil: mark the spot on each arm with pen, then cut\
`[img 2p1a]` `[img 2p1b]`

2.2) Assemble the spring, small dowel pin, & 3D printed clamp in the configuration shown in the image; do this twice\
`[img 2p2]`

2.3) Insert a M3×3mm×5mm brass threaded insert nut into the 3D-printed end plate near the square cutout\
`[img 2p3]`

2.4) Insert the 3D-printed button into the slot in the end plate\
`[img 2p4a]` `[img 2p4b]`

2.5) Insert the spring-dowel pin-clamp assemblies into the square cutout on the end plate. Note: if using a 3p end plate, must complete the battery build then fasten the end plate to the battery using two M3×16mm & two M3×5mm bolts before doing this step\
`[img 2p5a]` `[img 2p5b]`

2.6) Place 3D-printed cover over the square cutout, & fasten using M3×12mm bolt\
`[img 2p6a]` `[img 2p6b]`

---

## 3) Calculate Battery Busbar Size & Quantity

With the battery configuration specified by $MsNp$ where:
- $M$ = # of cells in series
- $N$ = # of cells in parallel

Then, we can properly specify the size & quantity of busbars required for the battery. Each battery requires two $1 \times N$ busbars for the positive & negative terminals. Additionally, each battery requires a quantity of $M-1$ busbars of size $2 \times N$.

For example, A battery that has 8 cells in series & 5 cells in parallel has a 8s5p configuration, so $M=8$ & $N=5$.

Thus, the battery requires:
Two busbars having size of $1 \times N = 1 \times 5$\
`[image of 1 x 5 busbar here]`

and busbars having size of $2 \times N = 2 \times 5$ in quantity of $M - 1 = 8 - 1 = 7$\
`[image of 2 x 5 busbar here]`

Finally, compute the total number of terminals on all busbars & then compute the number of busbar reels required (see BOM).

---

## 4) Prepare the Busbars

4.1) Compute size & quantity of the busbars required for the battery configuration

4.2) Cut out the busbars from the nickel-copper strip using metal shears. Each strip should terminate along the line where the nickel strips attach to the copper.\
`[img 4p2a]` `[img 4p2b]`

4.3) Cut off corners at 45° on each busbar & cut out notches approximately 4mm deep on either end of the wide busbars using metal shears\
`[img 4p3]`

4.4) Drill holes at the center of the four terminals at either end of each wide busbar using a hand drill or drill press with 5/16" or 8mm drill bit. First, mark the center-points on each busbar.\
`[img 4p4a]`

Then, attach busbars to a piece of scrap wood using double-sided tape (e.g. carpet tape)\
`[img 4p4b]`

Finally, drill the holes through each busbar\
`[img 4p4c]`

4.5) Solder 14 AWG solid copper wire along the edge of the narrow busbars\
`[img 4p5a]` `[img 4p5b]`

4.6) Solder female 6mm bullet connector to black & red 8 AWG wires having length of 40mm, then cover with shrink tube\
`[img 4p6a]` `[img 4p6b]`

4.7) Solder 8 AWG wires with connectors to the narrow busbars: mimic the images below.\
`[img 4p7]`

---

## 5) Place Cells in Frames & Spot Weld Busbars to Cells

5.1) Insert eight M3×4mm×5mm brass insert nuts into each frame part: four on top surface & two on each end\
`[img 5p1a]` `[img 5p1b]`

5.2) Put insulator rings on the positive terminals of all cells\
`[img 5p2]`

5.3) Insert cells into one frame: alternate the polarity along the long edge\
`[img 5p3]`

5.4) Fit the other frame over the cells: use mallet to seat in place if necessary\
`[img 5p4]`

5.5) Spot weld the wide busbars to the terminals: six spot welds per terminal is sufficient, with each spot weld pair made across the terminal cutout, not along it.
It helps to place dabs of super glue where the busbar makes contact with the plastic frame to hold the busbar in place.\
`[img 5p5a]` `[img 5p5b]` `[img 5p5c]`

> **NOTICE:** Test your spot welder settings on scrap metal before attempting to spot weld the busbars, since failed welds can lead to destroying the entire busbar...\
> `[img 5p5d]`

> Do a tug test to make sure the weld is secure.\
>`[img 5p5e]`

If you are using a battery-powered spot welder then I recommend that you charge up two batteries & switch off between them every ~60 welds to prevent them from overheating & exploding. Additionally, have a empty, sealable plastic container nearby: if the battery starts to swell, immediately unplug it, put it in the container, & take it outside for disposal.

Upon completion of this step, we can now define the side of the battery having only wide busbars as the "top side" of the battery.

5.6) Flip the battery over & place the thin busbars adjacent to their final positions: one w/ black wire near terminals w/ large exposed metal area, & one w/ red wire near terminals w/ insulator rings (see img)\
`[img 5p6]`

5.7) Glue down the narrow busbars above their intended weld points: place glue on the plastic areas that make contact w/ the copper, NOT on the terminals! Be careful to not make contact w/ the adjacent parallel cells as this will short the battery!\
`[img 5p7]`

5.8) Spot weld the narrow bus bars in place\
`[img 5p8]`

5.9) Glue down the remaining wide busbars in the open slots between the thin busbars, being careful not to make contact w/ adjacent parallel cells\
`[img 5p9]`

5.10) Spot weld the remaining terminals\
`[img 5p10]`

---

## 6) Wire-up the Power & Balance Connectors

6.1) Insert four threaded insert nuts into the bottom plate\
`[img 6p1]`

6.2) Position the battery on the edge of the bottom plate in the orientation seen in the image\
`[img 6p2]`

6.3) Separate the wires on the JST-XH connector (see image)\
`[img 6p3]`

6.4) With the red wire on the right, thread the upper wires through the holes along the bottom edge to the top side of the battery\
`[img 6p4a]` `[img 6p4b]`

6.5) Plug the JST-XH connector into its cutout in the bottom plate\
`[img 6p5]`

6.6) Pull each wire connected to the JST-XH connector lying on the bottom plate toward its respective busbar, then cut, strip, & solder it to the busbar

The solder points should be located below the bottom line of frame holes, with the wires oriented along the bottom edge (see image)\
`[img 6p6]`

6.7) With the battery still on the edge of the bottom plate, turn the battery around & solder the remaining balance wires to their respective terminals\
`[img 6p7]`

6.8) Solder MISTA 12-pin female connector to the battery board\
`[img 6p8a here]` `[img 6p8b here]`

6.9) Mount the board with connector into the bottom plate. Note that the batt. bottom plate must close with wires inside. Thus, for this to happen, the wires from the battery board must meet with those of the battery. In the mind's eye, project where the female bullet connectors on the battery wires would lie in the bottom plate if it were closed against the bottom of the battery. Cut an 8 AWG wire which extends from the battery board to this projected location, being mindful that the bullet connectors are aligned when connected.\
`[img 6p9 here]`

Then, cut the other wire using the length of this wire.
6.10) Solder male 6mm bullet connectors to the wires, then solder the wires to the batt. board: red to Vbatt+, black to Vbatt-\
`[img 6p10]`

Solder the wires to the batt. board s.t. they are at a 45° angle from sticking straight out, angled toward the side of the board w/o the notch in it.

6.11) Using a multimeter, check continuity between the Vbatt+ terminal & Vbatt- terminal on the batt. board. If no shorts found, then seat it in the bottom plate, secure with four M3×6mm screws, & plug it into the battery\
`[img 6p11]`

---

## 7) Attach Bottom, Top, & End Plates

7.1) Fasten the bottom plate to the battery bottom frame using four M3×16mm bolts & fasten the top plate to the battery top frame using four M3×8mm bolts.\
`[img 7p1 here]`

7.2) Fasten the assembled end plates to the ends of the battery using eight M3×16mm bolts, with four bolts used per end plate.\
`[img 7p2]`

*This concludes the battery build*

---

## 8) Battery Cell Voltage Check & First Charge-up

8.1) Connect the charging station with charger.\
`[img 8p1]`

8.2) Place battery on charging station, then check that each cell voltage is near 3.5V. If not, must rework the balance cable wiring: check the wiring on the charging station, & if issue isn't there then check the wiring within the battery.\
`[img 8p2]`

8.3) If each cell shows nominal voltages, either run balance charging (i.e., charge each cell to 3.75V) if putting it in storage or run ordinary charging (i.e., charge each cell to 4.1V) for immediate use.

> **Warning:** Set the charger battery type to LiIon, not LiPo!
