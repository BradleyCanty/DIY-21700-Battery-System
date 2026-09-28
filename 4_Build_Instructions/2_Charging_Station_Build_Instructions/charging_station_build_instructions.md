# Charging Station Build Instructions

## Outline
1. 3D print the parts
2. Assemble the charging station board
3. Assemble the charging station

---

## 1) 3D Print the Parts

| Part | Quantity | Filament | Print Settings |
| :--- | :--- | :--- | :--- |
| Charging station body | 1 | black ASA | 15% infill, requires 15mm outer brim |
| Charging station cover | 1 | black ASA | 15% infill |

---

## 2) Assemble the Charging Station Board

2.1) Place dab of super glue on bottom surface of MISTA 12 pin male connector & place on the charging station PCB, on the side w/ glue point labels\
<p align="center">
  <img src="Images/img_2p1.jpg" width="100%">
</p>

2.2) Place dab of super glue on bottom surfaces of two JST-XH 4-pin male connector & place on PCB. Ensure that the notches in the JST-XH connectors face toward the MISTA connector\
<p align="center">
  <img src="Images/img_2p2.jpg" width="100%">
</p>

2.3) Solder pins of MISTA & JST connectors to PCB\
<p align="center">
  <img src="Images/img_2p3.jpg" width="100%">
</p>

2.4) Solder the wires on the JST-XH male connector to the "balance wire" solder pads, starting with the red wire to "Vbatt" & proceeding in order to the final wire on "GND".\
<p align="center">
  <img src="Images/img_2p4.jpg" width="100%">
</p>

2.5) Cut black 12 AWG wire to 56 mm length & solder to 'batt-' terminal of antispark PCBA.\
<p align="center">
  <img src="Images/img_2p5.jpg" width="100%">
</p>

2.6) Cut black 12 AWG wire to 135 mm length & solder to 'load-' terminal of antispark PCBA.\
<p align="center">
  <img src="Images/img_2p6.jpg" width="100%">
</p>

2.7) Cut red 22 AWG wire to 80 mm length & solder to 'batt+' terminal of antispark PCBA.\
<p align="center">
  <img src="Images/img_2p7.jpg" width="100%">
</p>

2.8) Solder the short black 12 AWG wire from antispark PCBA to GND terminal on charging station board.\
<p align="center">
  <img src="Images/img_2p8.jpg" width="100%">
</p>

2.9) Cut red 12 AWG wire to 200 mm & solder to Vbatt terminal on charging station board.\
<p align="center">
  <img src="Images/img_2p9.jpg" width="100%">
</p>

2.10) Solder the other end of the red 22 AWG wire coming off the antispark PCBA to the charging station board's Vbatt terminal.\
<p align="center">
  <img src="Images/img_2p10.jpg" width="100%">
</p>

2.11) Pulling the red & black 12 AWG wire such that they are taut & parallel, then place heat shrink tube over the antispark circuit & shrink it down w/ heat gun.\
<p align="center">
  <img src="Images/img_2p11.jpg" width="100%">
</p>

2.12) Place heat shrink tube having 50mm length over the red & black 12AWG wires & shrink down.\
<p align="center">
  <img src="Images/img_2p12.jpg" width="100%">
</p>

2.13) If one of the 12 AWG wires is longer, then trim it to make them equal length. Then, solder XT60 connector, with red to + terminal & black to - terminal.\
<p align="center">
  <img src="Images/img_2p13.jpg" width="100%">
</p>

2.14) On the charging station board, place dabs of glue at the glue points and press the 3D printed cover to the surface. Let dry for ~30s.\
<p align="center">
  <img src="Images/img_2p14.jpg" width="100%">
  <img src="Images/img_2p15.jpg" width="100%">
</p>

*This concludes charging station board assembly*

---

## 3) Assemble the Charging Station

3.1) Insert the rounded dowel pins into the 3D printed charging station body.\
<p align="center">
  <img src="Images/img_3p1.jpg" width="100%">
</p>

3.2) Insert fully assembled charging station board into charging station body. Fasten using four M3x6mm bolts.\
<p align="center">
  <img src="4_Build_Instructions/2_Charging_Station_Build_Instructions/Images/img_3p2.jpg" width="100%">
</p>

*This concludes the charging station assembly*
